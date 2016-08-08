# Cookie Based Popup

Popups can ruin your site's user experience if implemented incorrectly but can serve as an excellent lead generation tool if used in the right way. [Solodev](https://www.solodev.com/) shows how using a cookie based popup can generate quality signups while maintaining a consistent user experience.

## Tutorial

For detailed instructions, view Solodev's [Adding a Cookie Based Form Popup to your Homepage](https://www.solodev.com/blog/web-design/adding-a-cookie-based-form-popup.stml) article.

## Demo

Check out a working example on [JSFiddle](https://jsfiddle.net/solodev/dpxttayx/).

## HTML

The popup form includes basic HTML markup:
```
<div id="popup-container">
   <div id="popup-window">
      <div class="modal-content">
         <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>  
         <a href="#" class="your-class"></a>
         <div>
            <div class="row text-center">
              <img src="assets/logo.png" />
            </div>
            <div class="row text-center">
              <h1>Newsletter Signup</h1>
              <p>Fill out the form below to signup for our weekly newsletter.</p>
            </div>
            <form action="" method="post" id="footer-form">
            <div class="row">
               <div class="col-md-6">
                  <label>First Name</label>
                  <input class="form-control" name="first_name" id="first_name" required>
               </div>
               <div class="col-md-6">
                  <label>Last Name</label>
                  <input class="form-control" name="last_name" id="last_name" required>
               </div>
            </div>
            <br>
            <div class="row">
               <div class="col-md-6">
                  <label>Email</label>
                  <input class="form-control" name="email" id="email" required>
               </div>
               <div class="col-md-6">
                  <label>Phone</label>
                  <input class="form-control" name="phone" id="phone">
                  <br>
               </div>
            </div>
            <input type="submit" class="btn btn-primary" value="Submit">
            </form>
            <br><br>
         </div>
      </div>
   </div>
</div>
```

## CSS

CSS for this repository is included in cookie-popup.css.

## JavaScript

jQuery is included in cookie-popup.js. The script checks to see if a cookie has been added and, if none is set, shows the popup form as demonstrated below:
```
if ( jQuery.cookie('visits') > 1 ) {
		jQuery('#active-popup').hide();
		jQuery('#popup-container').hide();
	} else {
			var pageHeight = jQuery(document).height();
			jQuery('<div id="active-popup"></div>').insertBefore('body');
			jQuery('#active-popup').css("height", pageHeight);
			jQuery('#popup-container').show();
	}
```

## External Includes

The form includes the following third-party resources:
```
<link href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" rel="stylesheet" type="text/css"/>
	
<script src="https://ajax.googleapis.com/ajax/libs/jquery/1.12.4/jquery.min.js" type="text/javascript" ></script>
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js" type="text/javascript" ></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/modernizr/2.8.3/modernizr.min.js" type="text/javascript" ></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery-cookie/1.4.1/jquery.cookie.js" type="text/javascript" ></script>
```
