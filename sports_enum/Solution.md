# Soltuion to create state machine for Sports enum using Method

```rust
// METHOD WAY (not associated function)

#[allow(dead_code)]
#[derive(Debug)]
enum Sports{
  Basketball, Volleyball, Football, Cricket,
}

impl Sports{
    fn change_sports(&mut self, change_to: Sports) {
     *self = change_to
    }
}

fn main() {
    let mut my_sport = Sports::Basketball;

    println!("{:#?}", my_sport);

    my_sport.change_sports(Sports::Volleyball);

    println!("{:#?}", my_sport);
}
```

## Notes
