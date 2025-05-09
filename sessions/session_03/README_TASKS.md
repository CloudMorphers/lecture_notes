# Your turn now!

<img src="https://media.giphy.com/media/13GIgrGdslD9oQ/giphy.gif" width=50%/>

  - [1) Implement an API for the simulator in your _ITU-MiniTwit_.](#1-implement-an-api-for-the-simulator-in-your-itu-minitwit)
  - [2) Continue refactoring of your ITU-MiniTwit.](#2\)-Continue-refactoring-of-your-ITU-MiniTwit.)


## 1) Implement an API for the simulator in your _ITU-MiniTwit_.


In two weeks, we will start a simulator that will run until the end of this course. It will simulate users interacting with your micro-blogging platform.

You can find the (*implicit*) specification for the simulator API in
[`API_Spec/minitwit_sim_api.py`](./API_Spec/minitwit_sim_api.py). **OBS**: your applications have to:

  - **Implement the same endpoints** (on different hosts of course and potentially different ports),
  - **Handle the same HTTP request types**, i.e., GETs and POSTs as specified with the same parameters and payloads as provided
  - Provide **the same HTTP status codes** in response as specified.


The [`API_Spec/minitwit_sim_api.py`](./API_Spec/minitwit_sim_api_test.py) depends on your refactored `minitwit.py` from last week's homework.

A corresponding test ([`API_Spec/minitwit_sim_api_test.py`](./API_Spec/minitwit_sim_api_test.py)) illustrates how the simulator requests will be formed. You can inspect it and run it via `pytest minitwit_sim_api_test.py`.
(`pytest` can be installed via `pip`)

Next to the unit test, there is a small program with some more test data, which is similar to the simulator program that will run against your systems. It is located in [`API_Spec/minitwit_simulator.py`](API_Spec/minitwit_simulator.py) and can be run via:

```bash
$ python minitwit_simulator.py http://localhost:5001
```

where the argument `http://localhost:5001` has to be replaced with the URL of where your simulator API is running. In case this simulator test does not log any errors, you should be all fine for next week. If errors are logged, you have to fix the corresponding issue either in your implementation of the simulator API or in the implementation of your version of _ITU-MiniTwit_.


| :exclamation:  **OBS**                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| We are talking about an API specification here. It is completely up to you how you integrate this into your systems. That is, that the program in `API_Spec/minitwit_sim_api.py` interacts directly with the database is only for illustration. It does not mean that the API has to be implemented like that in your systems! You will very likely want to factor out the common behavior between your endpoints that handle our simulator and your endpoints that render HTML. |


## 2) Continue refactoring and Deploy of your _ITU-MiniTwit_.

Continue refactoring of your version of _ITU-MiniTwit_ with missing features and added features of your liking.

### a) Deploy your _ITU-MiniTwit_ in "the cloud"

  * Deploy the current release of your _ITU-MiniTwit_, see task 2 b), to a remote ("cloud") server.
    - You might want to deploy to DigitalOcean, from where you get free credits from the GitHub education pack.
    - You might want to start with the exercise from the demo in the lecture, see slide [g) Automatic provision of remote clusters of virtual machines at DigitalOcean via Vagrant](./Slides.md#g-Automatic-provision-of-remote-clusters-of-virtual-machines-at-DigitalOcean-via-Vagrant).
    - **OBS**: The simulator API from the task above is considered part of your _ITU-MiniTwit_, i.e., it has to be deployed too.
  * **Do not** create and provision VMs manually, instead use a corresponding *script*, `Vagrantfile`, or a similar reproducible setup for that task.

  * You are free to deploy to whichever Infrastructure-as-a-Service (IaaS) provider of your choice or your own servers.
    - The only requirement is that your deployment is automatically reproducible, i.e., no clicking in UIs required, and that your application is reachable via a public IP/domain.
    - **Do not** deploy to a Platform-as-a-Service, like Heroku, Google App-Engine, etc.

  * Make your development environment and deployment environment "look alike". That is, you develop on an Ubuntu 22.04 based Linux (Pop!_OS), choose the same environment for your remote server(s).

  * **Hint**: To make future operations more smooth, you might **consider to use a [floating IP](https://docs.digitalocean.com/products/networking/floating-ips/) 'infront' of your actual server**, see the [API spec.](https://docs.digitalocean.com/reference/api/digitalocean/#tag/Floating-IPs) for receiving one.


**OBS MSc students**: Remember to log and provide good arguments for the choice of virtualization techniques and deployment targets.


### b) Release and deploy your _ITU-MiniTwit_.

  * Prepare a new release with the refactored version of your _ITU-MiniTwit_ latest by **Thursday Feb 20th, at 22:00**)
  * Send a pull request to `repositories.py` in our central repository: https://github.com/itu-devops/lecture_notes/blob/master/repositories.py
    - Add two URLs:
      * One to your running applications (edit `"http://<minitwit_application_url>"`)
      * Another one to the simulator API endpoint (edit `"http://<sim_api_url>"`)
