# cos418-assignment-2-chandy-lamport-distributed-snapshots-solved
**TO GET THIS SOLUTION VISIT:** [COS418 Assignment 2: Chandy-Lamport Distributed Snapshots Solved](https://www.ankitcodinghub.com/product/cos418-assignment-2-chandy-lamport-distributed-snapshots-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;53877&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;COS418 Assignment 2: Chandy-Lamport Distributed Snapshots Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (3 votes)    </div>
    </div>
<h2><a id="user-content-introduction" class="anchor" href="https://github.com/theoliao1998/Distributed-Systems/tree/master/2%20Chandy-Lamport%20Distributed%20Snapshots#introduction" aria-hidden="true"></a>Introduction</h2>
In this assignment you will implement the&nbsp;<a href="https://github.com/theoliao1998/Distributed-Systems/blob/master/2%20Chandy-Lamport%20Distributed%20Snapshots/papers/chandy_lamport.pdf">Chandy-Lamport algorithm</a>&nbsp;for distributed snapshots. Your snapshot algorithm will be implemented on top of a token passing system, similar to the ones presented in&nbsp;<a href="https://github.com/theoliao1998/Distributed-Systems/blob/master/2%20Chandy-Lamport%20Distributed%20Snapshots/docs/P4-distributed-snapshots.zip">Precept 4</a>&nbsp;and in the Chandy-Lamport paper.

The algorithm makes the following assumptions:

<ul>
<li>There are no failures and all messages arrive intact and only once</li>
<li>The communication channels are unidirectional and FIFO ordered</li>
<li>There is a communication path between any two processes in the system</li>
<li>Any process may initiate the snapshot algorithm</li>
<li>The snapshot algorithm does not interfere with the normal execution of the processes</li>
<li>Each process in the system records its local state and the state of its incoming channels</li>
</ul>
<h2><a id="user-content-software" class="anchor" href="https://github.com/theoliao1998/Distributed-Systems/tree/master/2%20Chandy-Lamport%20Distributed%20Snapshots#software" aria-hidden="true"></a>Software</h2>
You will find the code under this directory. The code is organized as follows:

<ul>
<li><tt>server.go</tt>: A process in the distributed algorithm</li>
<li><tt>simulator.go</tt>: A discrete time simulator</li>
<li><tt>logger.go</tt>: A logger that records events executed by system (useful for debugging)</li>
<li><tt>common.go</tt>: Debug flag and common message types used in the server, logger, and simulator</li>
<li><tt>snapshot_test.go</tt>: Tests you need to pass</li>
<li><tt>syncmap.go</tt>: Implementation of thread-safe map</li>
<li><tt>queue.go</tt>: Simple queue interface implemented using lists in Go</li>
<li><tt>test_common.go</tt>: Helper functions for testing</li>
<li><tt>test_data/</tt>: Test case inputs and expected results</li>
</ul>
Of these files, you only need to turn in&nbsp;<tt>server.go</tt>&nbsp;and&nbsp;<tt>simulator.go</tt>. However, some other files also contain information that will be useful for your implementation or debugging, such as the&nbsp;<tt>debug</tt>&nbsp;flag in&nbsp;<tt>common.go</tt>&nbsp;and the thread-safe map in&nbsp;<tt>syncmap.go</tt>. Your task is to implement the functions that say&nbsp;<tt>TODO: IMPLEMENT ME</tt>, adding fields to the surrounding classes if necessary.

<h3><a id="user-content-testing" class="anchor" href="https://github.com/theoliao1998/Distributed-Systems/tree/master/2%20Chandy-Lamport%20Distributed%20Snapshots#testing" aria-hidden="true"></a>Testing</h3>
Our grading uses the tests in&nbsp;<tt>snapshot_test.go</tt>&nbsp;provided to you. Test cases can be found in&nbsp;<tt>test_data/</tt>. To test the correctness of your code, simply run the following command:

<pre>  $ cd chandy-lamport/
  $ go test
  Running test '2nodes.top', '2nodes-simple.events'
  Running test '2nodes.top', '2nodes-message.events'
  Running test '3nodes.top', '3nodes-simple.events'
  Running test '3nodes.top', '3nodes-bidirectional-messages.events'
  Running test '8nodes.top', '8nodes-sequential-snapshots.events'
  Running test '8nodes.top', '8nodes-concurrent-snapshots.events'
  Running test '10nodes.top', '10nodes.events'
  PASS
  ok      _/path/to/chandy-lamport 0.012s
</pre>
To run individual tests, you can look up the test names in&nbsp;<tt>snapshot_test.go</tt>&nbsp;and run:

<pre>  $ go test -run 2Node
  Running test '2nodes.top', '2nodes-simple.events'
  Running test '2nodes.top', '2nodes-message.events'
  PASS
  ok      chandy-lamport  0.006s
</pre>
&nbsp;
