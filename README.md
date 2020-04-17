# module_platform_driver
  probe : msm_otg_driver

# 使用 DEVICE_ATTR()
  console path : /sys/devices/soc.0/78d9000.usb/dpdm_pulldown_enable

# 使用 msm_otg_register_power_supply()
   console path : ? (otg 相關)
   
# 使用 debugfs_create_dir 和 debugfs_create_file
   console path : /sys/kernel/debug/msm_otg
   對應 file_operations = [mode, chg_type, aca, bus_voting, otg_state]
   
# 使用 cdev_init()
  console path : ?
  對應 file_operations = [otg_ext_chg]
   
