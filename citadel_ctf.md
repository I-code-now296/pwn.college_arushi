# Zahard's Welcome
Flag: `citadel{7h3_c174d3l_b3ck0n5}`
- It was in rules channel description on discord

# The Social Network
Flag: `citadel{17_1s_jus7_7h3_b3g1nn1ng}`
- Went to instagram of citadweller and got half flag from highlight
- Then went to twitter (X whatever) and got other half from bio

# Omniscient Flag's Metadata
Flag: `citadel{th1s_ch4ll3ng3_1s_f0r_th4t_0n3_ex1ft00l_4nd_b1nw4lk_enthus14st}`
- Did `exiftools` on file
- Realised it has an image embedded from description in metadata
- Then extracted that through `binwalk`

  # Database Incursion
Flag: `citadel{wh3n_w1ll_y0u_f1nd_0u7_1f_175_5ql_0r_53qu3l?}`
- Realied with some internet search that I can use `--` to get rid of password
- So learnt a bit more SQL injection and used: `' OR 1=1 --` in username to get into daatabase
- Then I read the hints in notes and used: `' OR Department = 'Management' -- `
- I got pretty lost after this!

# Shinsu DEXquest
Flag: `citadel{f33ls_g00d_to_n0t_g3t_d33p_fr13d}`
- Installed JADX decompiler
- Decompiled the whole apk and went to com > shinsu.dexquest
- Found various places here, such as barrier, entrance etc.
- Went to vault and realised there were lot of numbers, combined them and found the number :`246451121036528202623890120011222498714684815355211850969748918921930947358058258074789422723982625`
- Installed the APK and inputted this in field where they ask for it, got a shinsu crystal
- This protected me and gave me the flag, which got copied to clipboard
