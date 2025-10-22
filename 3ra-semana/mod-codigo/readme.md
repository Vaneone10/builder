// Longitud excede en soroban ya que admite 9 ver documentación https://github.com/stellar/rs-soroban-sdk/blob/v23.0.2/soroban-sdk/src/symbol.rs
error: symbol too long: length 10, max 9
   --> src\lib.rs:494:28
    |
494 | ...   (symbol_short!("trnsfr_frm"), spender, from.clone(), to.clone()),

// No se usa Symbol, sacando esto deja de salir warning
warning: unused import: `Symbol`
 --> src\lib.rs:6:19
  |
6 |     symbol_short, Symbol

// env.events().publish Metodo deprecado en Version 23 de SDK, corregido en documento lib.rs
warning: use of deprecated method `soroban_sdk::events::Events::publish`: use th
e #[contractevent] macro on a contract event type
   --> src\lib.rs:151:22
    |
151 |         env.events().publish(
