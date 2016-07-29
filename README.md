# ArtCompany
<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
<html>
<head>
<title>arthur's portal</title>
<style> 
<cursor:url("smiley18.cur"); > </style>
<script src="captiveportal-prototype.js" type="text/javascript"></script>
<script src="captiveportal-scriptaculous.js" type="text/javascript"></script>
<script>
function guest(){
	if($('staffLogin').visible()){
		new Effect.BlindUp('staffLogin', {queue: {position:'end', scope: 'guestscope', limit:2} });
		new Effect.BlindDown('voucherSection', {queue: {position:'end', scope: 'guestscope', limit:2} });
	}
}

function staff(){
	if($('voucherSection').visible()){
		new Effect.BlindUp('voucherSection', {queue: {position:'end', scope: 'staffscope', limit:2} });
		new Effect.BlindDown('staffLogin', {queue: {position:'end', scope: 'staffscope', limit:2} });
	}
}

updateHelptext = function(){
	new Ajax.Updater('helpText', 'captiveportal-helptext.html', {method:'get'});
} 
    </script>
    <style type="text/css">
    body {
      background: url(captiveportal-bg_bubbles.jpg);
      background-color: #444;
      background: url(captiveportal-pinlayer2.png),url(captiveportal-pinlayer1.png),url();    
    }
    .vertical-offset-100 {
      padding-top:100px;
    }    
  </style>
    <style>
        .trans
        {
            width: 300px;
            text-align: center;
            background-color: Transparent;
            border-style: groove  ;
            border-top: none;
            border-left: dashed thin white;
            border-right: dashed thin white;
            border-bottom: dashed thin white;
            color: white;
            font-weight: bold;
            margin: auto;
        }
        img.clickimage
        {
            cursor: pointer;
        }
        .style1
        {
            background-color: #EE1B23;
        }
        .style2
        {
            background-color: #1E365C;
        }
        .style3
        {
            color: #FF9933;
        }
    </style>
    <meta  onload="text/html; charset=ISO-8859-1" http-equiv="content-type">
    <script src="captiveportal-jquery-1.11.1.min.js"></script>
</head> 
<body 
    color: rgb(0, 0, 0);" alink="#ee0000" link="#0000ee" vlink="#551a8b">
    <script src="captiveportal-tweenlite.min.js"></script>
    <div style="text-align: center; height:40px; width: 100%; top: 250px; position: absolute;
        left: 1px;">
        <form method="post" action="$PORTAL_ACTION$">
        <div style="height: 230px">
            <div onclick="guest()">
                <img style="" alt="" src="" class="clickimage" onclick="guest();"
                    value="">
            </div>
            <div id="voucherSection" align="center" style="width: 400px;" class="trans">
                <p2>
                    <font><font face="tunga"><span class="style2">Please enter your airtime</span><span class="style1"> 
                voucher code</span></font></p2>
                <br />
                    <font>
                <label for="Voucher">
                    <font face="tunga" color="White">Voucher:</font></label>
                <input name="auth_voucher" size="25" type="text">&nbsp;&nbsp;&nbsp;&nbsp;
                <p style="text-align: center;">
                    <input name="accept" type="submit" value="Login"></p>
                <br />
            </div>
            <div onclick="staff()">
                <img alt="" src="captiveportal-staff.png" class="clickimage" onclick="guest();">
            </div>
            <div id="staffLogin" style="display: none; width: 400px;" class="trans">
                <table style="">
                    <tr>
                        <td colspan="2">
                            <p>
                                <font><font face="tunga" color="white">Please enter your username and password</font></p>
                            <br />
                        </td>
                    </tr>
                    <tr>
                        <td>
                            <font><font face="tunga" color="white">Username:</font>
                        </td>
                        <td>
                            <input id="auth_user" name="auth_user" size="40" type="text">
                        </td>
                    </tr>
                    <tr>
                        <td>
                            <font><font face="tunga" color="white">Password:</font>
                        </td>
                        <td>
                            <input id="auth_pass" name="auth_pass" size="40" type="password">
                        </td>
                    </tr>
                    <tr>
                        <td colspan="2">
                            <p style="text-align: center;">
                                <input name="accept" type="submit" value="Login"></p>
                        </td>
                    </tr>
                </table>
            </div>
            <input name="redirurl" type="hidden" value="$PORTAL_REDIRURL$">
        </div>
        </form>
    </div>
    <div style="text-align: center; background-color: transparent;">
        <img style=" width: 967px; height: 716px; margin-top: -20px; margin-bottom: 0px; margin-right: 2px;" 
            alt="" src="captiveportal-bg_bubbles.jpg"
            align="middle"  ><br>&nbsp;<td>
                            <font><font face="tunga"><span class="style3">© www.fila.com.ph | All Rights Reserved 2016</span></font>
                        <span class="style3">
                        </td></span><br class="style3">
    </div>
</body>
</html>

