jQuery(document).ready(function($){

$("#afg_zipcode_form").submit(function(e) {

    e.preventDefault(); 
/*
    //var form = $(this);
var zipcode_value = $("#afg_PostalCode").val();
	alert(zipcode_value);
                 $.ajax({
                    type : "post",
                    url : api_req_zipcode.ajax_url,
                    data : {action: "api_req_zipcode", zipcode : zipcode_value},
                    success: function(response) { 
						//console.log(response);
						var result = JSON.parse(response);
						var result = JSON.parse(result.data);
						var data = result.data;
						if(data.length > 0){
						  console.log(data);
							data.forEach(function(item) {
								console.log(item);
								$("#get_res_content").html(item);
								$(".zip_id").html(item.id);
							});
						}
					}
				 });
                                 */
    
});
        

    $(document).on('change', '.zipcode_searchform .location_load_area select', function () {
		var val = $("option:selected", this).attr("url");
		console.log(val, "val");
        if (val != "" && typeof val !== "undefined") {
          val = val.split("https://locations.jovie.com.prod.rioseo.com")[1];
          val = window.location.origin + "/locations" + val;
          window.location.href = val + "#location-current-openings";
          // window.location.replace(window.location.origin+"/locations/?q=" + selected_location);
        }
    });
    
$(document).on('mouseup', '.force_cursor_placement input, .ginput_container input', function (e)
    {
        if (e.target.value.replace(/\(|\)|_|-|\./g, '').trim() == '')
        {
            e.target.setSelectionRange(0, 0);
        }

    });
    
/**
  // Gravity Forms  Disable Submission when Pressing Enter 
 */
$(document).on( 'keypress', '.gform_wrapper', function (e) {
    var code = e.keyCode || e.which;
    if ( code == 13 && ! jQuery( e.target ).is( 'textarea,input[type="submit"],input[type="button"]' ) ) {
        e.preventDefault();
        return false;
    }
} );  

$(".date_single_form").find("span").remove();
jQuery("#gform_submit_button_15").removeClass("disabled");
jQuery("#gform_submit_button_15").prop("disabled", false);


    /*zip code validate multistep forms js code start*/
    $(document).on('keyup change', '.location-input-validate input', function () {
        let zip_code = $(this).val();
        let  zip_code_val = zip_code.replace(/\D/g, '').length;
        console.log(zip_code_val);
        if (zip_code_val >= 5) {
            $(".gform_next_button").removeClass("disabled");
            $(".gform_next_button").prop("disabled", false);;
            
        } else {
            $(".gform_next_button").addClass("disabled");
            $(".gform_next_button").prop("disabled", true);
        }
    });
       $(document).on('blur', '.location-input-validate input', function () {
        let zip_code = $(this).val();
        let  zip_code_val = zip_code.replace(/\D/g, '').length;
        console.log(zip_code_val);
        if (zip_code_val >= 5) {
            
             setTimeout(function(){ $(".gform_next_button").removeClass("disabled");
            $(".gform_next_button").prop("disabled", false); }, 100);
        } else {            
             setTimeout(function(){
                 $(".gform_next_button").addClass("disabled");
                 $(".gform_next_button").prop("disabled", true);
        }, 100);
        }
    });
    /*zip code validate multistep forms js code end*/
});
        
// jQuery zoom in iphone website issue fixing code start

(function($) {
  var IS_IOS = /iphone|ipad/i.test(navigator.userAgent);
  $.fn.nodoubletapzoom = function() {
    if (IS_IOS)
      $(this).bind('touchstart', function preventZoom(e) {
        var t2 = e.timeStamp
          , t1 = $(this).data('lastTouch') || t2
          , dt = t2 - t1
          , fingers = e.originalEvent.touches.length;
        $(this).data('lastTouch', t2);
        if (!dt || dt > 500 || fingers > 1) return; // not double-tap

        e.preventDefault(); // double tap - prevent the zoom
        // also synthesize click events we just swallowed up
        $(this).trigger('click').trigger('click');
      });
  };
})(jQuery); 
// jQuery zoom in iphone website issue fixing code end 