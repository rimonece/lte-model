## 2009 Aug. 4 ##
  * modified files: checkin checkout dlairqueue.cc dls1queue.cc
  * dlairqueue.h
    * check flowcontrol is not triggered
    * timer is not triggered
    * bind the dnode

## 2009 July 29 HVQ (UE level) ##

  * int REDQueue::flow\_control()
    * if queue length < min, return -1;
    * else if packet drop is true, return 1; else return -1;
  * DLAirQueue::enque()
    * after the q3.enque(), p1=q3.flow\_control(), if p1==1; mark the HVQ\_UE
  * DLAirQueue::deque()
    * after the q3.deque(), p1=q3.flow\_control(), if p1==-1; demark the HVQ\_UE
  * DLS1Queue::deque()
    * before q3.deque(), if HVQ is marked, stop sending, try to send after some time.


## 2009 Jul. 7 ##
  * TBD
    * Send the paper for comments from the co-authors
  * Correct problems
    * The streaming traffic problem is caused by wrong defined default value of maximum packet number.
    * lte-model.doc Queue class is updated
    * the test results are got.

## 2009 Jul. 7 ##
  * TBD
    * Streaming traffic doesn't change with the simulation!!
    * lte-model.doc Queue class has some problem.
  * Correct problems
    * Queue limit