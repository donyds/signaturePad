# signaturePad
Create your own signature Pad using jQuery and HTML 


<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap 5 Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>.
  
  <style>
  
  .hd {
   background-image: url("https://img.freepik.com/free-vector/hand-painted-watercolor-pastel-sky-background_23-2148902771.jpg");
   }
  .as{
  background:#fff;
 }
  
  </style>
</head>
<body>

<div class="container-fluid p-5">
 <canvas class="hd"  id="signature" width="450" height="150" style="border: 1px solid #ddd;"></canvas>
<br>
<button id="clear-signature">Clear</button>
</div>

        
<script src="https://cdnjs.cloudflare.com/ajax/libs/signature_pad/1.5.3/signature_pad.min.js"></script>
<script src="https://code.jquery.com/jquery-2.2.3.min.js"></script>
<script>
jQuery(document).ready(function($){
    
    var canvas = document.getElementById("signature");
    var signaturePad = new SignaturePad(canvas);
    
    
    
    $('#clear-signature').on('click', function(){
        signaturePad.clear();
        
        
    });
    
      $('#signature').mousedown(function(){
    $(this).addClass('as');
  })
  
  
});
</script>



</body>
</html>
