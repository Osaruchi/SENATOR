# SENATOR
PIXEL ART MAKER PROJECT
My name is Kevin Green, populary called the Senator
I am an Engineer and i love to work with computer codes, that is why i join Udacity

<p>
<g-emoji class="g-emoji" alias="point_right" fallback-src="https://assets-cdn.github.com/images/icons/emoji/unicode/1f449.png">👉</g-emoji>
<a href= "https://github.com/Osaruchi/SENATOR.git/"rel="nofollow">View Online</a>
</p>


const canvas = $('#pixel_canvas');
const colorPicker = $('#colorPicker');
const linesOnOff = $('#grid_switch');
const eraser = $('#erase_grid');

// Select color input
// Select size input
var height, width, color;
// When size is submitted by the user, call makeGrid()
$('#sizePicker').submit(function (event){
  event.preventDefualt();
  height = $('inputHeight').val();
  width = $('inputWeight').val();
  makeGrid(height, width);
  // console.log('height:' + height + 'and width:' + width );
   

})

function makeGrid(x, y) {
screen('tr').remove()
// Your code goes here!
for (var i = 1; i<=x; i++) {
    $('#pixelCanvas').append('<tr id=table' + 1 + '></tr')
    for (var j = 1; i<=y; j++) {
      $('#table' +1).append('<td></td>');
    }
    } 
   // add color to cell
   $('td').click(function addcolor(){
     color = $('#colorPicker').val();

     if ($(this).attr('style')) {
       $(this).removeAttr('style')
     } else {
       $(this).attr('style', 'background-color:' + color);

     }
    
})
}
