!SLIDE small

    @@@ Ruby
    class Square
      def to_circle
      end
    end

    def CircleHole
    end

    CircleHole.new(Square.new.to_circle)

!SLIDE small
# Adapter pattern

!SLIDE small
    @@@ Ruby
    class Square
    end

    def SquareToCircle
      def adapt square
        circle(square)
      end
    end

    CircleHole.new
      SquareToCircle.new().adapt(Square.new)
