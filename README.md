# module_platform_driver
  probe : msm_otg_driver

# 使用 DEVICE_ATTR()
  console path : /sys/devices/soc.0/78d9000.usb/dpdm_pulldown_enable

# 使用 msm_otg_add_pdev()
  console path : /sys/bus/platform/devices
   
  對應 platform_device_add = [msm_hsusb, msm_hsusb_host]   
   
# 使用 debugfs_create_dir 和 debugfs_create_file
   console path : /sys/kernel/debug/msm_otg
   
   對應 file_operations = [mode, chg_type, aca, bus_voting, otg_state]
   
# 使用 cdev_init()
  console path : /sys/devices/virtual/msm_ext_chg
  
  對應 device_create = [usb_ext_chg]
  
# 使用 power_supply_property()
  console path : /sys/class/power_supply/usb
  
  對應 file_operations = [current_max, health, online, present, scope, type, voltage_max, voltage_now]
   
