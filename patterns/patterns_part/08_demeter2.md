!SLIDE small
    @@@ ruby
    def check_email
      user.account.login_email.is_valid?
    end
!SLIDE small
# Demeter law a.k.a Don't talk to Strangers
!SLIDE small
    @@@ ruby
    def check_email
      user.login_email.valid?
    end

    class User
      delegate :login_email, to: account
    end
