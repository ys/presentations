!SLIDE small
    @@@ ruby
    class User < ActiveRecord::Base

      def save
        super
        send_welcome_email
      end
    end

!SLIDE small
# Observer pattern
!SLIDE small
    @@@ ruby
    class User < ActiveRecord::Base
    end

    class UsrObserver < ActiveRecord::Observer
      observe :user
      def after_save(user)
        user.send_welcome_email
      end
    end
!SLIDE
<img src='http://blog.yannick.io/images/ruby.png'/>
