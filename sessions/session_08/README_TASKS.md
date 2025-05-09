-----------


# Your turn now!



## 1) Add Logging to Your Systems

Your task until next week is to add logging to your _ITU-MiniTwit_ systems.

You can deploy an EFK stack as we have shown in the exercises; but you can use also another logging stack.

It is ideal if you find a way to make the logging infrastructure available also to us. If you succeed, add the url of your logging dashboard to the `"Logging URL"` section of the `misc_urls.py` file. Make it accessible with the same credentials as the monitoring dashboard.


- Collect what you have done to fix issues with logging for later story in report
- Improve logging over time. Whenever you have the feeling you have an issue but you don't know the answer for it, it is likely a sign to improve logging with the right information.





## 2) Software Maintenance II

Check the user interface of another group's _ITU-MiniTwit_ application for functionality. That is, connect via a browser to another group's application and check if the system is working similar to the original _ITU-MiniTwit_, i.e.,

  * Do you see a public timeline?
  * Does the public timeline show messages that the application received from the simulator?
  * Can you create a new user?
  * Can you login as a new user?
  * Can you write a message?
  * After publishing a message, does it appear on your private timeline?
  * Can you follow another user?

In case you find non-functional/erroneous behavior please report it via issues to the respective GitHub repositories (find them in [`repositories.py`](https://github.com/itu-devops/lecture_notes/blob/master/repositories.py)).

**Do not** send requests to the simulator API of the other group. It is really only meant for the simulator (behave nicely towards the other group!). In case you want to make sure that non of the other groups sends requests to the simulator API of your group, you might want to only accept connections from the simulator server, which has the IP `104.248.134.203`.

Please find which group's user interface you are checking in the list below. Find your own group on the left-hand side and the name of the group your are checking behind the arrow. You will find the URL of the _ITU-MiniTwit_ application from the respective group in file [`repositories.py`](https://github.com/itu-devops/lecture_notes/blob/master/repositories.py) (first of the two given URLs).


### Who checks whom?

#### BSc

Group a - Group b

Group p - Group f

Group d - Group e

#### MSc

Group g - Group m

Group o - Group q

Group l - Group n

Group i - Group c

Group k - Group j

