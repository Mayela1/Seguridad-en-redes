### Descripción 
The Rust saga continues? I ask you, can I borrow that, pleeeeeaaaasseeeee?Download the Rust code [here](https://challenge-files.picoctf.net/c_verbal_sleep/babfbee79718a6363826ba86300173ffde6d81577e9dd07d4130c53a7eecf6c3/fixme2.tar.gz).
### Solución 
┌──(kali㉿kali)-[~/picoCTF/fixme2]
└─$ tar -xvzf fixme2.tar.gz            

fixme2/
fixme2/Cargo.toml
fixme2/Cargo.lock
fixme2/src/
fixme2/src/main.rs
 
┌──(kali㉿kali)-[~/picoCTF/fixme2]
└─$ cd fixme2

┌──(kali㉿kali)-[~/picoCTF/fixme2/fixme2]
└─$ cargo run
┌──(kali㉿kali)-[~/picoCTF/fixme2/fixme2/src]
└─$ nano main.rs
se xor_cryptor::XORCryptor;

fn decrypt(encrypted_buffer:Vec<u8>, borrowed_string: &mut String){ // How do>

    // Key for decryption
    let key = String::from("CSUCKS");

    // Editing our borrowed value
    borrowed_string.push_str("PARTY FOUL! Here is your flag: ");

    // Create decrpytion object
    let res = XORCryptor::new(&key);
    if res.is_err() {
        return; // How do we return in rust?
    }
    let xrc = res.unwrap();

    // Decrypt flag and print it out
    let decrypted_buffer = xrc.decrypt_vec(encrypted_buffer);
    borrowed_string.push_str(&String::from_utf8_lossy(&decrypted_buffer));
    println!("{}", borrowed_string);
}
fn main() {
    // Encrypted flag values
    let hex_values = ["41", "30", "20", "63", "4a", "45", "54", "76", "01", ">

    // Convert the hexadecimal strings to bytes and collect them into a vector
    let encrypted_buffer: Vec<u8> = hex_values.iter()
        .map(|&hex| u8::from_str_radix(hex, 16).unwrap())
        .collect();

    let mut party_foul = String::from("Using memory unsafe languages is a: ")>
    decrypt(encrypted_buffer, &mut party_foul); // Is this the correct way to>
}

┌──(kali㉿kali)-[~/picoCTF/fixme2/fixme2/src]
└─$ cargo run   
   Compiling rust_proj v0.1.0 (/home/kali/picoCTF/fixme2/fixme2)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.39s
     Running `/home/kali/picoCTF/fixme2/fixme2/target/debug/rust_proj`
Using memory unsafe languages is a: PARTY FOUL! Here is your flag: picoCTF{4r3_y0u_h4v1n5_fun_y31?}


### Notas adicionales
### Referencias