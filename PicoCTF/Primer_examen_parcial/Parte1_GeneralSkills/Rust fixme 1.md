### Descripción 
Have you heard of Rust? Fix the syntax errors in this Rust file to print the flag!Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/3f0e13f541928f420d9c8c96b06d4dbf7b2fa18b15adbd457108e8c80a1f5883/fixme1.tar.gz).
### Solución 
┌──(kali㉿kali)-[~]
└─$ curl https://sh.rustup.rs -sSf | sh

┌──(kali㉿kali)-[~]
└─$ source $HOME/.cargo/env

┌──(kali㉿kali)-[~/picoCTF/fixme1/fixme1]
└─$ ls
Cargo.lock  Cargo.toml  src  target

┌──(kali㉿kali)-[~/picoCTF/fixme1/fixme1]
└─$ cd src   
  
┌──(kali㉿kali)-[~/picoCTF/fixme1/fixme1/src]
└─$ cat main.rs 
──(kali㉿kali)-[~/picoCTF/fixme1/fixme1/src]
└─$ nano main.rs 
se xor_cryptor::XORCryptor;

fn main() {
    // Key for decryption
    let key = String::from("CSUCKS"); // How do we end statements in Rust?

    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", >

    // Convert the hexadecimal strings to bytes and collect them into a vect>
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    // Create decrpytion object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return; // How do we return in rust?
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    println!(

    
┌──(kali㉿kali)-[~/picoCTF/fixme1/fixme1/src]
└─$ cargo build
   Compiling rust_proj v0.1.0 (/home/kali/picoCTF/fixme1/fixme1)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.31s
         
┌──(kali㉿kali)-[~/picoCTF/fixme1/fixme1/src]
└─$ cargo run  
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.04s
     Running `/home/kali/picoCTF/fixme1/fixme1/target/debug/rust_proj`
picoCTF{4r3_y0u_4_ru$t4c30n_n0w?}:?

### Notas adicionales
### Referencias