# Урок 0. Hello World

## Теорія

- Cargo — менеджер пакетів, система збірки й тест-ранер Rust в одному інструменті; `Cargo.toml` — маніфест пакета: назва, версія, edition, залежності.
- Код програми лежить у `src/main.rs`, а виконання починається з функції `main`.
- `println!` друкує рядок у stdout і додає `\n`; знак `!` означає макрос, тому помилку в рядку формату ловить компілятор ще до запуску.
- `cargo run` збирає нативний бінарник у `target/debug/` в корені репозиторію й одразу запускає його — рантайм на кшталт `node` не потрібен.
- `cargo test` теж збирає програму, але запускає тести; файли з `tests/` — інтеграційні тести, які cargo знаходить сам.

## Приклад

```rust
fn main() {
    // println! is a macro: it writes the text and "\n" to stdout.
    println!("Rust says hi!");
}
```

## Порівняння з Node.js / NestJS

| Rust                         | Node.js / NestJS               |
|------------------------------|--------------------------------|
| `Cargo.toml`                 | `package.json`                 |
| `fn main()` у `src/main.rs`  | `bootstrap()` у `src/main.ts`  |
| `println!`                   | `console.log`                  |
| `cargo run`                  | `nest start`                   |
| `cargo test`                 | `jest`                         |
| `target/`                    | `dist/`                        |

## Завдання

Зміни лише `src/main.rs` так, щоб програма надрукувала в stdout рівно один рядок `Hello, world!`. Тести й `Cargo.toml` не чіпай.

## Перевірка

Запускай із папки уроку `lessons/000-hello-world/`; `cargo run` там само покаже, що друкує програма.
```sh
cargo test
```
