# Solution By Jere

```rust
#[allow(dead_code)]
#[derive(Debug)]
enum Sports {
    Basketball,
    Volleyball,
    Football,
    Cricket,
}

impl Sports {
    fn change_sports(&mut self, change_to: Sports) {
        *self = change_to
    }
}

fn main() {
    let mut current_sport = Sports::Basketball;

    println!("{:?}", current_sport);

    current_sport.change_sports(Sports::Volleyball);

    println!("{:?}", current_sport);
}
```

## Notes

