!SLIDE small
    @@@ ruby
    class Bank
      def deposit *args
      end
    end

    check_access_to_bank
    bank.deposit 50, '$'
!SLIDE small
#Proxy pattern
!SLIDE small
    @@@ ruby
    class BankEmployee
      def initialize(bank)
        @bank = bank
      end

      def deposit total
        check_access
        @bank.deposit total, *args1
      end
    end

    bankEmployee.deposit 50
