## From [[Garston Liang]] / [[Paul Garrett]] in May 2023

How to capture tab events when using [[jsPsych]] to recognise when someone is leaving the experiment prior to completion.

```javascript
on_interaction_data_update: function(data){
    if(data.event == "blur" & troubleshooting == false){
        if(!studyFinished){
            tab_exits = tab_exits + 1
            alert("Please do not leave the experiment prior to completion & ensure the browser is in full-screen mode (F11).")
        }
    }
}
```

Note that tab_exists is just a variable starting at 0

Troubleshooting is for my debugger – can delete

Blur is an interaction event to say they looked away (focus is a return event)

StudyFinished is a logical to say if the tab alert should trigger on a given trial (can set to false within a variable – like a stim event – by using the on_finish or on_start commands; see next code cell where there is a retention interval where the tab monitoring is turned off at the end, and is turned on with ‘on_start’ on the next stimulus response even

```javascript
var retention_interval = {
    type: jsPsychHtmlKeyboardResponse,
    stimulus: '',
    choices: 'NO_KEYS',
    trial_duration: DisplayTime[ii],
    data: {trial_event: 'fixation'},
    on_finish: function(data){ // Turn back on tab monitoring
        studyFinished = false
    }
}
```