# Sport enum solution with both method and associated function

```rust
#![allow(dead_code)]

#[derive(Debug)]
enum Sport {
    Basketball,
    Volleyball,
    Football,
    Cricket,
}

// METHOD
impl Sport {
    fn change_sport(&mut self, new_sport: Sport) {
        *self = new_sport;
    }
}

// ASSOCIATED FUNCTION
impl Sport {
    fn associate_sport(current_sport: &mut Sport, new_sport: Sport){
        *current_sport = new_sport;
    }
}

fn main() {
    let mut current_sport = Sport::Football;

    println!("{:?}", current_sport);

    current_sport.change_sport(Sport::Basketball);

    println!("{:?}", current_sport);

    Sport::associate_sport(&mut current_sport, Sport::Volleyball);

    println!("{:?}", current_sport);
}
```

## Notes

1. The asssiated function is associated with TYPE, not with instance of the type.

    > `Sport::associate_sport`

2. The method is associated with instance of the type.

    > `current_sport.change_sport(Sport::Basketball);`

3. Both method and associated function can be used to change the state of the enum from one variant to another.
