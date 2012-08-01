!SLIDE small
    @@@ ruby
    class DbConnectionPool
      def initialize
      end
    end

    DbConnectionPool.new
!SLIDE small
#Singleton pattern
!SLIDE small
    @@@ ruby
    class DbConnectionPool
      def instance
        @@instance ||= DbConnectionPool.new
      end
      private_class_method :new
    end

    DbConnectionPool.instance
!SLIDE
<img src='http://blog.yannick.io/images/ruby.png'/>
