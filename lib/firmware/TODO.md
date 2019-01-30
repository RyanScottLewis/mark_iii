
  # TODO THIS DOESNT EXIST YET, atm everything is pragmatically generated
  drv_register(
    table(
      "name"="btn",
      "types"=array("gmod_wire_button", "gmod_wire_dynamic_button"),
    )
  )

  # Once dev_registerAll is called, should now have vfs files
  # > assuming: @inputs Dev0:wirelink Dev1:wirelink
  # > and Dev0 is connected to a button
  # > and Dev1 is connected to a console screen
  #
  # /sys/devices/0/name # => "Dev0"
  # /sys/devices/0/type # => "gmod_wire_button"
  # /sys/devices/0/driver -> /sys/class/btn/btn0/
  # /sys/class/btn/btn0/name # => "btn"
  # /sys/class/btn/btn0/value # => Current button value
  # /sys/class/btn/btn0/device -> /sys/devices/0/
  #
  # /sys/devices/1/name # => "Dev1"
  # /sys/devices/1/type # => "gmod_wire_consolescreen"
  # /sys/devices/1/driver -> /sys/class/cs/cs0/
  # /sys/class/cs/cs0/name # => "cs"
  # /sys/class/cs/cs0/value # => Write only, prints text directly to screen
  # /sys/class/cs/cs0/device -> /sys/devices/1/
