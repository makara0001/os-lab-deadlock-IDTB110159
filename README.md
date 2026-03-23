![image](Screenshot%20From%202026-03-23%2014-40-07.png)

The output of `df -h | grep loop` confirms that the image files were successfully attached as loop devices and mounted as file systems. This demonstrates that regular files can function as virtual storage devices in Linux.

![image](Screenshot%20From%202026-03-23%2014-40-13.png)

![image](Screenshot%20From%202026-03-23%2014-43-05.png)

The deadlock occurs due to a circular wait condition:

- `sync_up` locks **Vault Alpha** and waits for **Vault Beta**
- `sync_down` locks **Vault Beta** and waits for **Vault Alpha**

![image](Screenshot%20From%202026-03-23%2014-59-38.png)

Explanation  
This demonstrates a distributed deadlock where two users each hold a lock and wait for the other. This simulates a distributed denial-of-service scenario, where independent systems block each other and halt overall progress.
