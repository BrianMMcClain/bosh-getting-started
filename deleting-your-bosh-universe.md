# Clean up! Deleting your BOSH universe

You've created a BOSH, you played with it and deployed environments. How do you clean up? (That is, how do you stop paying AWS for all your tutorial VM?!)


After cleaning up your BOSH created VMs, lastly you delete your BOSH VM:

```
$ fog
  Welcome to fog interactive!
  :default provides AWS and VirtualBox
connection = Fog::Compute.new({:provider => 'AWS'})
connection.servers.last.destroy
connection.addresses.last.destroy
connection.key_pairs.last.destroy
```

TODO - make this more advanced. Perhaps setup VMs with tags etc.