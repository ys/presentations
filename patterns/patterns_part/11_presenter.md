!SLIDE small
    @@@ ruby
    class User
      def access_list_by_month
        Access.where(user: self.id)
          .group(:month)
      end
    end
!SLIDE small
# Presenter pattern
!SLIDE small
    @@@ ruby
    class UserPresenter
      def initialize(user)
        @user = user
      end

      def access_list
        Access.where(user: @user.id)
      end

      def access_list_by_month
        access_list.group(:month)
      end
    end
