<div id="Codice 1-sortableTrash" class="sortable-code"></div> 
<div id="Codice 1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Codice 1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="Codice 1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "x = int(input(&quot;Dammi un numero: &quot;))
\n" +
    "for i in range(0, x, 1):
\n" +
    "    c+= i
\n" +
    "print(c)
\n" +
    "x += y
\n" +
    "#distractor
\n" +
    "i - x
\n" +
    "#distractor
\n" +
    "printa(a)
\n" +
    "#distractor
\n" +
    "for j in y:#distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Codice 1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "python3": true,
    "trashId": "Codice 1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Codice 1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Codice 1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
