# SweetKit

Some handlers for MotionKit that add the coercion abilities of SugarCube to the
style abilities of MotionKit, for great good.

    $ gem install sweet-kit
    gem 'sweet-kit'

# Styles

See styles.rb for helper methods.

```ruby
class AnyLayout < MK::Layout
  include SweetKit::Styles

  def text_field_styles
    sweetkit_input
    # =>
    font :system.uifont(14)
    color :black
    border :rounded
    alignment :left
    opaque false
    backgroundColor :clear
  end

end
```
# Shadow

```ruby
add UIView do
  shadow do  # also works in a CALayer context
    opacity 0.5
    radius 5
    offset [1, 2]
    color :gray
    path UIBezierPath.bezierPathWithRoundedRect([[0, 0], [100, 100]], cornerRadius: 5)
  end
end
```

