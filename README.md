// Edit By Meux VR
var _title = '<title>.💕کτγℓع❥ー�</title>';
$('title').replaceWith(_title);
//$('body').append('<div id="minimapContener"><canvas id="minimap" width="200" height="200" style="pointer-events:none;background:rgba(59, 59, 84, 0.22);position:absolute;bottom:10px;right:10px;border:rgba(59, 59, 84, 0.50) 2px solid; z-index:2"></canvas></div>');


// Makrolar
var SplitInterval;
var MacroInterval;
var SplitDebounce = false;
var MacroDebounce = false;
$(document).on('keydown', function(input) {
    console.log("got keydown")
    if (input.keyCode == 84) {
        if (SplitDebounce) {
            return;
        }
        SplitDebounce = true;
        SplitInterval = setInterval(function() {
            $("body").trigger($.Event("keydown", {
                keyCode: 32
            }));
            $("body").trigger($.Event("keyup", {
                keyCode: 32
            }));
        }, 0);
    } else if (input.keyCode == 69) {
  if (MacroDebounce) {
            return;
        }
        MacroDebounce = true;
        MacroInterval = setInterval(function() {
            $("body").trigger($.Event("keydown", {
                keyCode: 87
            }));
            $("body").trigger($.Event("keyup", {
                keyCode: 87
            }));
            $("body").trigger($.Event("keyup", {
                keyCode: 87
            }));
            $("body").trigger($.Event("keyup", {
                keyCode: 87
            }));
        }, 0);
 }
})
 
$(document).on('keyup', function(input) {
    if (input.keyCode == 84) {
        SplitDebounce = false;
        clearInterval(SplitInterval);
        return;
    } else if (input.keyCode == 69) {
        MacroDebounce = false;
        clearInterval(MacroInterval);
        return;
    }
})


// Other
