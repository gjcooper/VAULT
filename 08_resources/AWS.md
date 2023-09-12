# AWS

## Initial Thoughts / Process

tmux/git now installed by default

```sh

git clone <https://github.com/gjcooper/dotfiles.git>
cd dotfiles
python3 scripts/managehome.py \~/dotfiles --config git --links --setup vim ohmyzsh

git clone <https://github.com/gjcooper/gcphd-model_of_dce.git>

sudo yum install zsh sudo yum install util-linux-user chsh
```

1.  Update pmwg/mcce

```sh
sudo yum install harfbuzz-devel fribidi-devel
sudo yum groupinstall "Development Tools"
```

```r
install.packages('devtools')
devtools::install\_github("university-of-newcastle-research/pmwg",
ref="extra\_info")
```

\> Log off and on again or source .zshrc
```r
devtools::install\_github('gjcooper/gcphd-model\_of\_dce')
```

1.  Finalise data

```sh
cd gcphd-model\_of\_dce
cp \~/studies/PreferentialDCE/Pref\_preprocessed.RDS data/output/.
```

## Helpful global commands

### Get creds

> EC2 -\> `okta-awscli -o uon-res-swb S3` -\> `okta-awscli -o > uon-res-swb_s3`

### Instance cmds

```sh
aws ec2 describe-instances | jq '
\[ .Reservations\[\].Instances\[\] |
select(.Tags\[\] |
contains({Key: "CreatedBy", Value: "gjc216"})) |
{ ID: .InstanceId, State: .State, Name: (.Tags\[\] |
if .Key == "ServiceWorkbenchName" then .Value else empty end) } \]'
```

### S3 Commands

```sh
for bucket in \((aws s3 ls s3://418071489834-prod-syd-uonswb-egress-store/ | awk '{ print \)2; }') do
    echo $bucket aws s3 ls s3://418071489834-prod-syd-uonswb-egress-store/$bucket 2> /dev/null
done
```

## Preferential DCE

#### Log in:

Reduced:
`aws ssm start-session --target i-068dc8f24099951a4`

ReducedMore:
`aws ssm start-session --target i-0cfc3bc49eaa1b503`

Normal:
`aws ssm start-session --target i-073e794196e1e5158`

### Access s3 bucket

#### View files:

`aws s3 ls s3://418071489834-prod-syd-uonswb-egress-store/189fa174-3bd8-40c0-a722-d93c41c19ea0/`

#### Get files:

`aws s3 cp s3://418071489834-prod-syd-uonswb-egress-store/189fa174-3bd8-40c0-a722-d93c41c19ea0/X ./X`

## Playground

### Log into instance:

#### Log in:

`aws ssm start-session --target i-0e3bef37211b99f39`

Null-Estimator
`aws ssm start-session --target i-0425f42ecdb4a653f`

## Tutorial Paper

Log into instances:

<span id="Smaller instance"></span>**Smaller instance**
`./start-session.sh gjc216 278440638476 i-0d5a4dc5d0612e4aa`
<span id="32 CPUs"></span>**32 CPUs**
``./start-session.sh gjc216 278440638476 i-0425f42ecdb4a653f`

<span id="Get Data"></span>**Get Data** 
`./assume-role.sh gjc216 418071489834`

`aws s3 cp s3://418071489834-prod-syd-uonswb-egress-store/15c9ffa9-850b-4373-ae6d-f4efdbbbb991/Model2_Null.RData ~/coding/school\_work/samplers/tutorial\_test/.``
