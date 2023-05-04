Download Link: https://assignmentchef.com/product/solved-cs520-computer-architecture-project-1
<br>
<h1>1. RULES</h1>




<ul>

 <li>All students must work alone. Cooperation is not allowed.</li>

 <li>Sharing of code between students is considered cheating and will receive appropriate action in accordance with University policy. The TAs will scan source code through various tools available to us for detecting cheating. Source code that is flagged by these tools will be dealt with severely.</li>

 <li>You must do all your work in the C/C++.</li>

 <li>Your code must be compiled on remote.cs.binghamton.edu or the machines in the EB‐G7 and EB‐Q22. This is the platform where the TAs will compile and test your simulator. They all have the same software environment.</li>

</ul>




<ol start="2">

 <li><strong> Project Description</strong></li>

</ol>




In this project, you will construct a baking pipeline simulator.

<strong> </strong>

<h1>3. Baking Pipeline Simulator</h1>




The baking simulator has the following 12 stages.







<table width="623">

 <tbody>

  <tr>

   <td width="102">Stage</td>

   <td width="522">Description</td>

  </tr>

  <tr>

   <td width="102">Scaling</td>

   <td width="522">All ingredients are measured and lined up in order of use.</td>

  </tr>

  <tr>

   <td width="102">Mixing</td>

   <td width="522">Ingredients are combined into a dough.</td>

  </tr>

  <tr>

   <td width="102">Fermentation</td>

   <td width="522">The dough is allowed to ferment.</td>

  </tr>

  <tr>

   <td width="102">Folding</td>

   <td width="522">The dough is folded to be degassed.</td>

  </tr>

  <tr>

   <td width="102">Dividing</td>

   <td width="522">The dough is divided into the desired individual portions.</td>

  </tr>

  <tr>

   <td width="102">Rounding</td>

   <td width="522">The portioned dough is loosely shaped into round balls.</td>

  </tr>

  <tr>

   <td width="102">Resting</td>

   <td width="522">The dough is rested for a while to relax the gluten</td>

  </tr>

  <tr>

   <td width="102">Shaping</td>

   <td width="522">The dough is formed into its final shape.</td>

  </tr>

  <tr>

   <td width="102">Proofing</td>

   <td width="522">The dough goes through one final fermentation.</td>

  </tr>

  <tr>

   <td width="102">Baking</td>

   <td width="522">The dough is baked.Note. The oven needs to be cleaned for 1 minute after every 10 baking.</td>

  </tr>

  <tr>

   <td width="102">Cooling</td>

   <td width="522">The loaves are cooled on racks.</td>

  </tr>

  <tr>

   <td width="102">Stocking</td>

   <td width="522">The baked bread is placed on shelves.</td>

  </tr>

 </tbody>

</table>




The baking pipeline receives one request at every minute. Suppose that every stage needs 1 minute except the baking stage. Note that the scaling stage takes a 10‐minute break after every 1000 requests to prepare new materials. Also, the baking stage needs a 1‐minute break after every ten baking. If the stage takes a break, the stage is stalled, and all the requests need the stage must wait until it becomes available again.




Unlike other stages, the baking stage needs 1 or 2 minutes, depending on the bread type. A bagel needs 1‐minute baking, and a baguette needs 2‐minute baking at the baking stage.




The no‐request is there to inject a bubble into the pipeline. Thereby, even though the pipeline stage is stalled, the bubble still can proceed. For example, during the scaling stage’s break, no‐request operations can still be read from the trace file.




The simulator receives one request among three request types as follows every minute.




&gt; No‐Request

&gt; Bake‐Bagel

&gt; Bake‐Baguette




The request traces (trace1, trace2, trace3, and trace4) are already provided. You must complete your projects in the provided project01.c and project01.h files. <strong>You cannot add extra files.</strong>




<h1>4. Validation and Other Requirements</h1>




<h2>4.1. Validation requirements</h2>




Sample simulation outputs are provided. You must run your simulator and debug it until it matches the simulation outputs. Your simulator must print the final results correctly as follows.




Baking count:

‐ Bagel baking:

‐ Baguette baking:

No request:




How many minutes to bake:




Performance (bakes/minutes):




Your output must match both numerically and in terms of formatting, because the TAs will “diff” your output with the correct output. You must confirm correctness of your simulator by following these two steps for each program:




<ul>

 <li>Redirect the console output of your simulator to a temporary file. This can be achieved by placing “&gt; your_output_file” after the simulator command.</li>

</ul>




<ul>

 <li>Test whether or not your outputs match properly, by running this unix command: “diff –iw &lt;your_output_file&gt; &lt;posted_output_file&gt;”</li>

</ul>




The –iw flags tell “diff” to treat upper‐case and lower‐case as equivalent and to ignore the amount of whitespace between words. Therefore, you do not need to worry about the exact number of spaces or tabs as long as there is some whitespace where the sample outputs have whitespace. Both your outputs and final memory_map.txt must be the same as the solution.




<ul>

 <li>Your simulator must run correctly not only with the given traces. Note that TA will validate your simulator with hidden traces.</li>

</ul>




<h2>4.2. Compiling and running simulator</h2>




You will hand in source code and the TA will compile and run your simulator. As such, you must be able to compile and run your simulator on machines in EB‐G7 and EB‐Q22. This is required so that the TAs can compile and run your simulator. You also can access the machine with the same environment remotely at remote.cs.binghamton.edu via SSH.




The pipeline receives a program name.




e.g. ./baking_sim traces/trace1 &gt; results/traces/output_trace1




<h1>5. What to submit</h1>




You must hand in project1.c. Also, you must submit a cover page with the project title, the Honor Pledge, and your full name as electronic signature of the Honor Pledge. A cover page is posted on the project website.




<h1>6. Penalties</h1>




Various deductions (out of 100 points):

<strong>‐5 points</strong> for each date late during the first 6 days.

<strong>‐10 points</strong> for each date late after the first 6 days.




<strong>Up to ‐10 points</strong> for not complying with specific procedures. Follow all procedures very carefully to avoid penalties.




<strong>Cheating</strong>: Source code that is flagged by tools available to us will be dealt with according to University Policy. This includes a 0 for the project and other disciplinary actions.


