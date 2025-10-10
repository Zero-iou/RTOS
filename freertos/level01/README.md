## You can use this command to program the board
openocd -f openocd_dap.cfg -c init -c halt -c "program build/Debug/task_manager_led.hex" -c reset -c shutdown

