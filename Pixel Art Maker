@@ -1,10 +1,34 @@
-// Select color input
-// Select size input
-
-// When size is submitted by the user, call makeGrid()
+/*
+Input: no input
+Output: no output
+Behavior: change current scope background color to the color picked from colorPicker
+*/
+function changeColor() {
+    const color = document.getElementById("colorPicker").value;
+    this.style.background = color;
+}
 
-function makeGrid() {
 
-// Your code goes here!
 
-}
+/*
+Input: no input
+Output: no output
+Behavior : It creates a table with width and height from input. Each cell contains 
+            onclick event handler that calls changeColor() function.
+            After the event, the behavior stays without going to default.
+*/
+function makeGrid() {
+    const gridHeight = document.getElementById("input_height").value;
+    const gridWidth = document.getElementById("input_width").value;
+    const pixelCanvas = document.getElementById("pixel_canvas"); 
+    pixelCanvas.innerText=""; // empty table   
+    
+    for (let h=0; h<gridHeight; ++h) {
+        const row = pixelCanvas.insertRow(-1); // insert new row at the last position
+        for (let w=0; w<gridWidth; ++w) {
+            const cell = row.insertCell(-1); //insert new cell at the last position
+            cell.onclick = changeColor;
+        }
+    }
+    event.preventDefault();
+}
5 index.html
@@ -9,7 +9,7 @@
     <h1>Lab: Pixel Art Maker</h1>
 
     <h2>Choose Grid Size</h2>
-    <form id="sizePicker">
+    <form id="sizePicker" onsubmit="makeGrid()">
         Grid Height:
         <input type="number" id="input_height" name="height" min="1" value="1">
         Grid Width:
@@ -21,7 +21,8 @@ <h2>Pick A Color</h2>
     <input type="color" id="colorPicker">
 
     <h2>Design Canvas</h2>
-    <table id="pixel_canvas"></table>
+    <table id="pixel_canvas">
+    </table>
 
     <script src="designs.js"></script>
 </body>
