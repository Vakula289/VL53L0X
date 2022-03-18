import time
import VL53L0X
import matplotlib.pyplot as plt
import matplotlib.animation as animation

tof = VL53L0X.VL53L0X()
tof.start_ranging(VL53L0X.VL53L0X_BETTER_ACCURACY_MODE)

x,y =[], []
while True:
    D = tof.get_distance()
    
    print(D)
    time.sleep(0.05)
    
    # fig = plt.figure()
    # ax = fig.add_subplot(1, 1, 1)
    # xs = []
    # ys = []

    # def animate(i, xs, ys):

    # # Add x and y to lists
    #     xs.append(dt.datetime.now().strftime('%H:%M:%S.%f'))
    #     ys.append(temp_c)

    # # Limit x and y lists to 20 items
    #     xs = xs[-20:]
    #     ys = ys[-20:]

    # # Draw x and y lists
    #     ax.clear()
    #     ax.plot(xs, ys)

    # # Format plot
    #     plt.xticks(rotation=45, ha='right')
    #     plt.subplots_adjust(bottom=0.30)
    #     plt.title('TMP102 Temperature over Time')
    #     plt.ylabel('Temperature (deg C)')


    dcm = D/10

    if dcm<50:
        print("Obstacle at a distance of:",dcm)
        print("Haptic Alert sent to belt!!")
