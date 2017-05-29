# snapshotmgr
EBS Snapshot Manager (to view / delete AWS EBS Snapshot)

#Requirements

- [NodeJS](http://nodejs.org/)

#Installation/Setup

    git clone <this repo>
    npm install

#Options
- profile : (optional) Loads the profile from ~/.aws/credentials. If not specified, loads the 'default' profile. For details on how to configure the profiles, see [here](http://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-multiple-profiles)
- action : (optional) Acceptable values are 'list','delete' . Default : 'list'
- region : (optional) Valid AWS Regions (more [here](http://docs.aws.amazon.com/general/latest/gr/rande.html#cfn_region))
- filterByStatus : (optional) Valid Snapshot Stack Statuses (more [here](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html)). Specify more than one status separated by commas. If not specified, cf-manager will attempt to list stacks of all statuses.
- pattern : (optional) A string pattern that the name(s) of EBS Snapshot(s) begin with. If not specified, snapshotmgr will attempt to list all snapshots.
- beforeTime : ISO 8601 timestamp
- afterTime : ISO 8601 timestamp
- findByVolumeId : AWS EBS Volume Id , find snapshots related to a specific volume
- help : (optional) Display a helpful usage message

#Example usage

    snapshotmgr --pattern foo-bar- --filterByStatus completed --action delete
The above command will list all snapshots that start with "foo-bar-" and with status 'completed' and will request input for deletion

# Bugs

Please report bugs [here](https://github.com/ivarrian/snapshotmgr/issues)
