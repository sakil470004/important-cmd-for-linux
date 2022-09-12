  <h1>Enable and disable input device like keyboard</h1>
    <hr />
    <ol>
        <li>We are using "xinput" here</li>
        <li>To enable or disable device we need device name or id</li>
        <li>We can see it by using "xinput list"</li>
        <li>To disable device cmd "xinput disable "device_name" [which device you want to disable]</li>
        <li>To enable device cmd "xinput enable "device_name" [which device you want to enable]</li>
    </ol>
    <h3>Here is the example of some code which automated for this task by using "bash" </h3>
    <pre>
      <code>
        #!/bin/bash
        Icon="/home/mynul/.config/keybordShortcut/icon/keyboardon.png"
        Icoff="/home/mynul/.config/keybordShortcut/icon/keyboardoff.png"
        fconfig=".keyboard" 
        devicename="Logitech USB Keyboard"
        id=$(xinput list --id-only "$devicename")
        
        
        if [ ! -f $fconfig ]; then
          echo "Creating config file"
          echo "enabled" > $fconfig
          var="enabled"
        else
          read -r var< $fconfig
          echo "keyboard is : $var"
        fi
        
        if [ "$var" = "disabled" ]; then
          notify-send -i $Icon "Enabling keyboard..." \ "ON - Keyboard connected !";
          echo "enable keyboard..."
          xinput enable $id
          echo "enabled" > $fconfig
        elif [ "$var" = "enabled" ]; then
          notify-send -i $Icoff "Disabling Keyboard" \ "OFF - Keyboard disconnected";
          echo "disable keyboard"
          xinput disable $id
          echo 'disabled' > $fconfig
        fi
  </code>
</pre>
<h4>Here "Logitech USB Keyboard" is my keyboard name </h4>
<hr/>
<ol>
<li>To run the bash file 1st save copy code as 'test.sh' </li>
<li>Run the file using this command 'bash test.sh'</li>
</ol>
