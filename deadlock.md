![image](Pasted%20image%2020260323153517.png)

The output of `df -h | grep loop` confirms that the image files were successfully attached as loop devices and mounted as file systems. This demonstrates that regular files can function as virtual storage devices in Linux.

![image](Pasted%20image%2020260323153700.png)

![image](Pasted%20image%2020260323153722.png)

The deadlock occurs due to a circular wait condition:

- `sync_up` locks **Vault Alpha** and waits for **Vault Beta**
- `sync_down` locks **Vault Beta** and waits for **Vault Alpha**

![image](Pasted%20image%2020260323153809.png)

Explanation  
This demonstrates a distributed deadlock where two users each hold a lock and wait for the other. This simulates a distributed denial-of-service scenario, where independent systems block each other and halt overall progress.
