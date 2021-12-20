# [Forest](https://app.hackthebox.com/challenges/forest)

Stego challenge

## Requirements

- [Java](https://adoptium.net/?variant=openjdk11)
- [Dcode](https://www.dcode.fr/)
- [Stegsolve](http://www.caesum.com/handbook/Stegsolve.jar)
- Steghide Linux

  ```
  sudo apt install steghide
  ```

## Solution

- Unzip with

    ```
    unzip forest.zip
    ```
- We get an image. We can change the aspects of the image with stegsolve.

    ```
    java -jar stegsolve.jar
    ```
    
    and import the image.
    
- At red plane 0 we see a code appear.

    IsJuS1Af0r3sTbR0

- We use the code to exctract whatever is in the image.

    ```
    steghide extract -sf forest.jpg
    ```
- We get a file nothinghere.txt we look inside and we get encrypted text.

     ```
    cat nothinghere.txt
    ``` 
    
    Gur sberfg vf n pbzcyrk rpbflfgrz pbafvfgvat znvayl bs gerrf gung ohssre gur rnegu naq fhccbeg n zlevnq bs yvsr sbezf. Gur gerrf uryc perngr n fcrpvny raivebazrag juvpu, va ghea, nssrpgf gur xvaqf bs navznyf naq cynagf gung pna rkvfg va gur sberfg. Gerrf ner na vzcbegnag pbzcbarag bs gur raivebazrag. Gurl pyrna gur nve, pbby vg ba ubg qnlf, pbafreir urng ng avtug, naq npg nf rkpryyrag fbhaq nofbeoref. UGO{NzNm1aTfXvyYmMOe0}
                                                                                   
    
- We see that is an anagram so we use dcode Ceazar Cipher. The +13 is the right option and we get a text.

	The forest is a complex ecosystem consisting mainly of trees that buffer the earth and support a myriad of life forms. The trees help create a special environment which, in turn, affects the kinds of animals and plants that can exist in the forest. Trees are an important component of the environment. They clean the air, cool it on hot days, conserve heat at night, and act as excellent sound absorbers. HTB{AmAz1nGsKilLzZBr0}

- Flag: HTB{AmAz1nGsKilLzZBr0}
