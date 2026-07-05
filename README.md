# Riz Heritage — Deploy Kaise Karein

Ye pura static site hai (HTML/CSS/JS) — koi build step nahi chahiye, isiliye seedha zip drag-and-drop se live ho jayega.

## Deploy (Netlify)
1. Is folder ke andar ke saare files+folders (index.html, css/, js/, about.html, etc.) ko zip karo — folder ko khud zip mat karo, uske andar ka content zip karo.
2. Netlify.com pe login karo → "Add new site" → "Deploy manually" → zip drag-drop karo.
3. Site turant live ho jayega, ek random URL milega — chaho to Site settings mein custom name daal sakte ho.

Vercel aur Cloudflare Pages pe bhi same tarah drag-and-drop se deploy ho jayega.

## Zaroori: Real photos daalna mat bhoolna
Saare images abhi `picsum.photos` ke random placeholder hain — sirf layout dikhane ke liye. Live hone se pehle in sab ko Riz Heritage ke real photos (hotel rooms, restaurant, palace decoration) se replace karna hoga:
- Har `<img src="https://picsum.photos/...">` ko apni photo ke path se replace karo, e.g. `images/room1.jpg`
- Photos ko `images/` folder mein daal do aur path update kar do.

## Contact details update karna
Abhi phone number `+91 12345 67890` aur email `info@rizheritage.com` placeholder hain. Ye files mein find-and-replace karo (sabhi 7 HTML files mein):
- Phone number: search `911234567890` (WhatsApp/call links) aur `+91 12345 67890` (display text)
- Email: search `info@rizheritage.com`
- Google Map: `contact.html` aur `index.html` mein map iframe ka query "Shahabad, Hardoi" hai — apni exact location/pin daalne ke liye Google Maps pe jaake apna address search karo, "Share" → "Embed a map" se naya embed link lo.

## Contact form
Form abhi sirf demo hai (koi backend nahi) — submit karne par sirf "thank you" message dikhta hai, kahin bhejta nahi. Agar real enquiries chahiye to Formspree ya Netlify Forms jaisi free service add karni hogi — bata dena, wo bhi set kar dunga.

## Files
- `index.html` — Home
- `about.html` — About
- `hotel.html` — Hotel Rooms
- `restaurant.html` — Restaurant
- `palace.html` — Riz Palace (wedding venue)
- `gallery.html` — Gallery (filterable)
- `contact.html` — Contact + enquiry form
- `css/style.css`, `js/script.js` — shared styling & interactions
