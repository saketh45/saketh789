<!DOCTYPE html>
<html>
    <head>
        <title>
            adding and removing Notes
        </title>
        <script src="https://code.jquery.com/jquery-3.5.1.js" 
        integrity="sha256-QWo7LDvxbWT2tbbQ97B53yJnYU3WhH/C8ycbRAkjPDc=" 
        crossorigin="anonymous"></script>
        
    </head>
    <body>
        <body> 
            <h1>
                add notes
            </h1>
            <br><br>
             <ul> 
                <li>add sample notes like this</li>
                 
                 
            </ul>
            <br><br>
            <div id="newitemButton">
                <button href="#" id="showForm">new note</button>
            </div> 
                <form id="newitemForm"> 
                <input type="text" id="itemDescription" placeholder="Add description .. . " />
                 <input type="submit" id="addButton" val ue"'"add" / > </form>  
                   
                    <script type="text/javascript">
                       $(function() {  
                           var  $newitemButton=$('#newitemButton');                     
                           var $newitemForm = $('#newitemForm') ; 
                           var $textinput = $('input:text'); 
                            $newitemButton.show(); 
                            $newitemForm.hide(); 
                            $('#showForm').on('click', function() {
                                 $newitemButton.hide(); 
                                 $newitemForm.show();
                                  }) ; 
                            $newitemForm.on( ' submit',function(e){ 
                                e.preventDefault(); 
                                var newText = $('input:text') .val ();
                                 $('li:last') .after('<li>' + newText + '</li>'); 
                                 $newitemForm.hide() ;
                                  $newitemButton.show(); 
                                  $textinput.val( ' ' ); 
                                  }) ; 
                                }) ;  
                        
                    </script>  
    </body>
</html>
