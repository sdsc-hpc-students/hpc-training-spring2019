# HPC Training: Spring 2019
Week 8: Friday, May 26th, 2019

## TOPIC: An Introduction to Cloud Computing
Presented by: Dr. Martin Kandes (mkandes@sdsc.edu)

## READING AND PRESENTATIONS:
* [Training Presentation](./introduction-to-cloud-computing.pdf)

## REFERENCES:
* [Jetstream User Guide](https://portal.xsede.org/jetstream)
* [Jetstream Public Wiki](https://iujetstream.atlassian.net/wiki/spaces/JWT/overview)
* [OpenStack Homepage](https://www.openstack.org)
  [HTCondor Manual](https://htcondor.readthedocs.io/en/v8_8_3)

## TASKS:
0. Setup access to the jetstream cloud:
1. Spin up an m1.tiny instance at IU using the Openstack Horizon GUI. 
2. Install HTCondor on this instance and configure it as a Personal HTCondor pool.
3. Run the bash_pi.htcondor job on your Personal HTCondor pool.
4. Reconfigure your instance to be an HTCondor execute node and have it join the shared HTCondor pool. 
5. Once your execute node has joined the pool, login to the HTCondor submit node and run bash_pi.htcondor again. 
