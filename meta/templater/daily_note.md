---
created: <% tp.file.creation_date() %>
---

# <% moment(tp.file.title,'YYYY-MM-DD').format("dddd, MMMM DD, YYYY") %>

---

### Daily Summary

#### Work

##### Planned work

- [ ] 

##### Extra work achieved

-  

#### Personal

##### Planned Activities

- [ ] 

##### Extra achievements

-  

---

# Temporary Notes

- 

---
### Notes created today
```dataview
List FROM "" WHERE file.cday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.ctime asc
```

### Notes last touched today
```dataview
List FROM "" WHERE file.mday = date("<%tp.date.now("YYYY-MM-DD")%>") SORT file.mtime asc
```
---

###### Tags

#dailyNote
