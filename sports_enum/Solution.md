# Soltuion to create state machine for Sports enum using Method

```rust
// METHOD WAY (not associated function)

#![allow(dead_code)]

#[derive(Debug)]
enum Sports{
  Basketball, Volleyball, Football, Cricket,
}

impl Sports{
    fn change_sport(&mut self, new_sport: Sports) {
     *self = new_sport
    }
}

fn main() {
    let mut current_sport = Sports::Basketball;

    println!("{:#?}", current_sport);

    current_sport.change_sport(Sports::Volleyball);

    println!("{:#?}", current_sport);
}
```

## Notes
