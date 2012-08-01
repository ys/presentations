!SLIDE small
    @@@ Ruby
    class Downloader; def download; end end
    class Archiver; def archive; end end

    class DelayedJobRunner
      def run
        while queue.has_tasks
          task = queue.get_first
          case task.class
          when Downloader
            task.download
          when Archiver
            task.archiver
          end
        end
      end
    end

!SLIDE small
# Command pattern

!SLIDE small

    @@@ Ruby
    class Downloader; def execute; end end
    class Archiver; def execute; end end

    class DelayedJobRunner
      def run
        while queue.has_tasks
          queue.get_first.execute
        end
      end
    end
!SLIDE
<img src='http://blog.yannick.io/images/ruby.png'/>
