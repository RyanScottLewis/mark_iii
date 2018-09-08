# Eos BIOS
> Eos - Greek Titaness of the dawn.

## Features

* Programmable power-on, self-test (POST)
  * Reporting
    * Beep code reporting
    * Output device (console screen, light, etc)

## Boot process

* Register all connected devices
* POST, if enabled
* Run the default executable

## POST

On boot, the system performs a POST which checks for input and output devices (the "IO" in "BIOS")
along with as other common problems. After the POST, errors are reported with a series of beeps, as
well as any output devices.

### Beep codes

If the computer fails the POST, the following beep codes will be generated:

#### Legend

Character    | Description
-------------|------------
`.` (period) | Short beep
`-` (hyphen) | Long beep

#### Codes

Code | Description
-----|------------
`.`  | POST successful
`..` | No input devices
`.-` | No output devices
`-`  | No input or output devices

#### Configuration

```ruby
# Getter/setter for enabling POST entirely
# Default: 1
number eos_post_enabled()
void   eos_post_enabled(Value:number)

# Getter/setter for checking for input devices
# Default: 1
number eos_post_checkInputs()
void   eos_post_checkInputs(Value:number)

# Getter/setter for checking for output devices
# Default: 1
number eos_post_checkOutputs()
void   eos_post_checkOutputs(Value:number)

# Getter/setter for the list of valid input device types
# If set to empty array, all device types will be valid.
# Default: array() # Empty
array  eos_post_validInputs()
void   eos_post_validInputs(DeviceTypes:array)

# Getter/setter for the list of valid output device types
# If set to empty array, all device types will be valid.
# Default: array() # Empty
array  eos_post_validOutputs()
void   eos_post_validOutputs(DeviceTypes:array)

# Getter/setter for reporting the "POST successful" single short beep
# Default: 1
number eos_post_reportSuccessBeep()
void   eos_post_reportSuccessBeep(Value:number)

# Getter/setter for reporting errors to all connected console screens
# Default: 1
number eos_post_reportToCS()
void   eos_post_reportToCS(Value:number)
```
