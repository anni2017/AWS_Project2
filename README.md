🚀 SMART AWS COST SAVER – AUTO-CLEANUP OF OLD SNAPSHOTS

Ever wondered why your AWS bill keeps growing even when you’re not using all your servers?
That’s often because of old EBS snapshots — backup copies of your data that just sit there, unused, still costing money.

How it works (in simple terms):

The Lambda function first gets all EBS snapshots in your account.
Then it checks all EC2 instances that are still active (either running or stopped).
For each snapshot, it verifies whether the volume it belongs to is still linked with any active EC2 instance.
If not, it means the snapshot is no longer in use, so the function deletes it to free up space and save money.
