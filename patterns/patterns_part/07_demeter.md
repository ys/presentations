!SLIDE small
    @@@ ruby
    def check_for_overheating(system_monitor)
      if system_monitor.temperature > 100
        system_monitor.sound_alarms
      end
    end
    
!SLIDE small
# Just know which object do what
!SLIDE small
    @@@ ruby
    system_monitor.check_for_overheating

    class SystemMonitor
      def check_for_overheating
        if temperature > 100
          sound_alarms
        end
      end
    end
!SLIDE
<img src='http://blog.yannick.io/images/ruby.png'/>
