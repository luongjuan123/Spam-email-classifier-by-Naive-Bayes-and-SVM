# SMS Spam Collection v.1

## 1. Description

The **SMS Spam Collection v.1** (hereafter the corpus) is a set of SMS tagged messages collected for SMS Spam research. It contains **5,574 English SMS messages**, labeled as either:

- **ham** (legitimate)
- **spam**

---

## 1.1 Compilation

This corpus was compiled from various free or research-available web sources:

- **Grumbletext Website**
  - ~425 spam messages manually extracted
  - Source: http://www.grumbletext.co.uk/
  - Notes: Required careful scanning of user complaints

- **Caroline Tagg's PhD Thesis**
  - 450 ham messages
  - Source: http://etheses.bham.ac.uk/253/1/Tagg09PhD.pdf

- **NUS SMS Corpus (NSC)**
  - 3,375 ham messages
  - Collected from students at the National University of Singapore
  - Source: http://www.comp.nus.edu.sg/~rpnlpir/downloads/corpora/smsCorpus/

- **SMS Spam Corpus v.0.1 Big**
  - 1,002 ham messages
  - 322 spam messages
  - Source: http://www.esp.uem.es/jmgomez/smsspamcorpus/

---

## 1.2 Statistics

- **Total messages:** 5,574
- **Ham (legitimate):** 4,827 (86.6%)
- **Spam:** 747 (13.4%)

---

## 1.3 Format

- One message per line
- Each line contains:
  - Label (`ham` or `spam`)
  - Message text

### Example:

ham What you doing?how are you? \
ham Ok lar... Joking wif u oni... \  
ham dun say so early hor... U c already then say... \ 
ham MY NO. IN LUTON 0125698789 RING ME IF UR AROUND! H* \ 
ham Siva is in hostel aha:-. \
ham Cos i was out shopping wif darren jus now n i called him 2 ask wat present he wan lor... \
spam FreeMsg: Txt: CALL to No: 86888 & claim your reward... \
spam Sunshine Quiz! Win a super Sony DVD recorder... \
spam URGENT! Your Mobile No was awarded a £2,000 Bonus...  \


> **Note:** Messages are not chronologically sorted.

---

## 2. Usage

A comprehensive study of this corpus is described in:

> Almeida, T.A., Gómez Hidalgo, J.M., Yamakami, A.  
> *Contributions to the study of SMS Spam Filtering: New Collection and Results.*  
> Proceedings of the 2011 ACM Symposium on Document Engineering (DOCENG'11).

---

## 3. About

The corpus was collected by:

- Tiago Agostinho de Almeida  
  http://www.dt.fee.unicamp.br/~tiago  

- José María Gómez Hidalgo  
  http://www.esp.uem.es/jmgomez  

Special thanks to:

- Dr. Min-Yen Kan and team (NUS SMS Corpus)  
  http://www.comp.nus.edu.sg/~kanmy/

Additional dataset:
- http://wing.comp.nus.edu.sg:8080/SMSCorpus/

---

## 4. License / Disclaimer

### Usage Guidelines

- Please cite the dataset if used in research:
  http://www.dt.fee.unicamp.br/~tiago/smsspamcollection/
- Notify authors via: tiago@dt.fee.unicamp.br

---

### Legal Terms

1. **Copyright**
   - Owned by Tiago A. de Almeida and José M. Gómez Hidalgo

2. **No Warranty**
   - Provided *"as is"* without any guarantees
   - Users assume all risks

3. **Limitation of Liability**
   - Authors are not responsible for:
     - Data loss
     - Commercial damages
     - Any indirect or consequential issues

---

## Summary

-  5,574 SMS messages  
-  86.6% ham  
-  13.4% spam  
-  Widely used for spam detection research  


