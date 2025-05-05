# ee425-lab-3-interrupt-service-routine-isr-solved
**TO GET THIS SOLUTION VISIT:** [EE425 Lab 3-Interrupt Service Routine (ISR) Solved](https://www.ankitcodinghub.com/product/ee425-lab-3-interrupt-service-routine-isr-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;95147&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;EE425 Lab 3-Interrupt Service Routine (ISR) Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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

<div class="kksr-stars-active" style="width: 0px;">
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
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Experiment 3 – Interrupt Service Routine (ISR)

Objective: This experiment is designed to show: the handling capabilities of interrupts of the PIC18F4520 microcontroller; and the ability of students to manipulate the behavior of the microcontroller. Use the microchip to detect external interrupts using the appropriate controller pins.

Preliminaries:

<ul>
<li>This experiment will use the “P3_template.asm” that has been provided to you.</li>
<li>In this experiment you will use the Logic Analyzer embedded in the IDE—please see my MPLAB IDE Tutorial which
shows how to set it up and how to use it. Do not proceed further in this assignment until you know how to use the

Logic Analyzer.
</li>
<li>Add the channels RC2, RC1, RB0, RE2, RB1, RA1, RA2, RA3 to the Logic Analyzer window and let the animation
run for some time. Your Logic Analyzer window should look as in Figure 1:

Figure 1. Pulse train at bit RC2.
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
• Click on Debugger &gt;&gt; Stimulus&gt;&gt; New Workbook. This will launch a new window called Stimulus. The rows of cells in this new window will be empty, but you can then populate one cell at the time by clicking on it and adding the appropriate signal that corresponds to an external stimulus. Add pins RB1, RB0, and RE2 to so that your Stimulus window looks as in Figure 2. You must make sure that the Action and Width settings for each pin are the same as show in the figure. You may add comments as in the right column in order to make testing easier later.

Figure 2. External stimuli signals.

Specific Tasks: The microcontroller should be programmed in a way that it executes the following tasks

(READ CAREFULLY):

Please note the following items must be programmed into a single .asm file.

<ol>
<li>Write code to set INT0 (bit RB0 in PORTB) as you High Priority Interrupt and INT1 (bit RB1 in PORTB) as your Low Priority Interrupt. These bits will correspond to the external, asynchronous signals that will be used as your interrupt trigger signals in order to execute an interruption of the mainline program. RB0 and RB1 will be monitored from the Logic Analuzer window shown in Figure 1, but they will be triggered from the Stimulus in Figure 2. RE2 is an additional external input signal that will be applied (or triggered) by the human programmer or program user—we will call this RE2 asynchronous signal the Human Input Signal. During the animation of the main program, whenever you want to trigger (or fire) an interrupt event on either RB0, RB1, or RE2, click on the corresponding Fire button to the left of each signal in the Stimulus window, and then see what happens on the Logic Analyzer window.</li>
<li>Write assembly code to implement the following interrupt event hierarchy.</li>
</ol>
a. As the mainline program, that is, the program that will be interrupted using the external interrupts, let the bit

RC2 of PORTC output a periodic pulse train with duty cycle=50% and a half-period of 0.1ms. This pulse 2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
train in the mainline must run indefinitely unless an interrupt is triggered. Please note that this pulse train is already being generated in the P3_template.asm.

<ol start="2">
<li>When an asynchronous low priority (LP) interrupt event occurs, that is, when you trigger or fire the interrupt signal RB1 from the Stimulus window, the following actions must take place:
<ul>
<li>The bits RA1, RA2, and RA3 of PORTA must begin stepping through the sequence shown in the table
below. The sequence must first count up from STEP 1 to STEP 8. You must program a 0.2ms delay in between steps.

STEP RA3 RA2 RA1

<ol>
<li>1 &nbsp;on on on</li>
<li>2 &nbsp;on on off</li>
<li>3 &nbsp;on off on</li>
<li>4 &nbsp;on off off</li>
<li>5 &nbsp;off on on</li>
<li>6 &nbsp;off on off</li>
<li>7 &nbsp;off off on</li>
<li>8 &nbsp;off off off</li>
</ol>
</li>
<li>All other activities must stop: pulse train from pin RC2 must be stopped (cleared) so that it is RC2 is LOW for as long as the LP-ISR is running.</li>
<li>Upon returning to the main program, bits RA1, RA2, and RA3 of PORTA must be cleared and the pulse train from pin RC2 must resume execution.</li>
<li>You must trigger the Low Priority Interrupt signal, RB1, from the Stimulus window to test the functionality of this LP-ISR.</li>
</ul>
</li>
<li>When an asynchronous high priority (HP) interrupt event occurs, that is, when you trigger or fire the interrupt signal RB0 from the Stimulus window, the following actions must take place:</li>
</ol>
<ul>
<li>The pulse train from bit RC2 must be cleared and the bits RA1, RA2, and RA3 of PORTA must be also cleared.</li>
<li>The HP-ISR must then enter into an indefinite loop. In order to leave the indefinite loop, write a breaking condition that
is dependent upon the Human Input Signal coming from bit RE2. That is, the indefinite loop must break only when RE2 = 1, otherwise the indefinite loop will continue to run until human input is sensed. You should trigger the Human Input Signal, RE2, from the Stimulus window to test the functionality of your breaking condition.
</li>
<li>You must trigger the High Priority Interrupt signal, RB0, from the Stimulus window to test the functionality of this HP- ISR.</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
