<!DOCTYPE html PUBLIC "-//WAPFORUM//DTD XHTML Mobile 1.0//EN" "http://www.wapforum.org/DTD/xhtml-mobile10.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" lang="en">
    <head>
<meta charset="UTF-8">
<link rel="icon" href="//www.microsoft.com/favicon.ico" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CEK DA, PA, SS, BL, ALEXA, UMUR DOMAIN</title>
<link rel="stylesheet" href="//cdn.jsdelivr.net/bootstrap/4.0.0-alpha.5/css/bootstrap-flex.min.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/bootstrap/4.0.0-alpha.5/css/bootstrap-grid.min.css" />
<link href="//fonts.googleapis.com/css?family=Play" rel="stylesheet">
       <style>
body { max-width: 700px; position: relative; background: white center center fixed; margin: auto; margin-top: 20px; cursor: auto; font-family: Play; font-size: 16px; padding: 7px; }
h2 { text-decoration: uppercase; font-weight: bold; }
h1 { margin: 3px; padding: 3px; text-align: center; }
h2, h3, h4, h5 { font-size: 18px; text-align: left; }
table, td, tr { border: none }   
input, select, option, input[type=text], input.btn { border: 1px solid #ccc; padding: 5px; }
table.table td { border: 1px solid #a6a6a6; padding: 5px; text-align: center; }
tr.ths { background: #a4bdfc; color: #532f00; font-weight: bold; text-align: center; }
input, select, option, input[type=text], input.btn { border: 1px solid #ccc; padding: 5px; }
.domains { text-align: center; color: blue; font-weight: bold; padding: 5px; margin: 0 0 4px 0; border: 1px solid #a6a6a6; }
      </style>
</head>
    <body>
        <h1>AUTHORITY</h1>
        <hr />
        
            <center>
        <form method="post">
            <input type="text" name="domain" placeholder="domain.com" />
            <input type="submit" value="SUBMIT" />
        </form>
            </center>
            
<?php

    $domain = trim($_POST[domain]);
    $key = '-API-KEY-DISINI-';
    $limit = '5'; // INI LIMIT LIST BACKLINK, ISI ANTARA 1-50
    
        if($domain){
            $data = json_decode(file_get_contents('https://seo.sulsel.go.id/api.cgi?key='.$key.'&domain='.$domain), true);
            $back = json_decode(file_get_contents('https://seo.sulsel.go.id/backlink.cgi?key='.$key.'&domain='.$domain.'&limit='.$limit), true);
            echo '<p></p>
                <div class="domains">
            <font style="font-size: 26px">
                <font color="black">&hearts;</font> 
                '.$domain.'
                <font color="black">&hearts;</font>
            </font>
                </div>
                
                <table class="table" style="margin: 0 0 4px 0;" align="center">
        <tr class="ths">
        <td>HISTORI</td>
        <td>DAFTAR</td>
        <td>EXPIRED</td>
        </tr><tr>
        <td>'.$data[hi].'</td>
        <td>'.$data[reg].'</td>
        <td>'.$data[exp].'</td>
        </tr>
                </table>
                
                <table class="table" style="margin: 0 0 4px 0;" align="center">
        <tr class="ths">
        <td>DA</td>
        <td>PA</td>
        <td>SS</td>
        <td>BACKLINK</td>
        <td>ALEXA</td>
        </tr><tr>
        <td>'.$data[da].'</td>
        <td>'.$data[pa].'</td>
        <td><b style="color:Green">'.$data[ss].'</b></td>
        <td>'.$data[bl].'</td>
        <td>'.$data[agr].'</td>
        </tr>
                </table>';
        
        if(count($back) > 0){
           echo '<table class="table">
                <tr class="ths">
                <td>TOP '.$limit.' SUMBER BACKLINK</td>
                <td>D A</td>
                </tr>';
            foreach($back as $link){
                echo '<tr>
                <td style="text-align:left">'.$link[ref].'</td>
                <td align="center"><b style="color:green">'.$link[da].'</b>/<font color="blue">100</font></td>
                </tr>';
            }
            echo '</table>';
        }
                
        }


?>
    <!-- MAU PASANGIN IKLAN ATAU MACAM MACAM ? LETAKKAN DISINI -->
    
    </body>
        </html>
