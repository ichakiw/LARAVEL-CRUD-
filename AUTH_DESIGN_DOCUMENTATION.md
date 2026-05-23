# 🎨 Warung Online - Auth Design System

Dokumentasi lengkap untuk design system halaman Login & Register yang modern dan menarik.

## 📋 Isi Perubahan

### Halaman yang Diubah
1. **Login Page** - `resources/views/auth/login.blade.php`
2. **Register Page** - `resources/views/auth/register.blade.php`
3. **Guest Layout** - `resources/views/layouts/guest.blade.php`
4. **CSS Auth** - `resources/css/auth.css` (file baru)

### Komponen yang Diupdate
- `resources/views/components/auth-session-status.blade.php`
- `resources/views/components/input-error.blade.php`

## 🎯 Design Highlights

### Color Palette
```
Primary Color:     #667eea (Ungu)
Dark Primary:      #764ba2 (Ungu Gelap)
Success:           #10b981 (Hijau)
Error:             #ef4444 (Merah)
Background:        #f9fafb (Abu-abu Muda)
Border:            #e5e7eb (Abu-abu Sedang)
```

### Typography
- Font Family: `Poppins` (modern & clean)
- Heading: Bold (700), 24-32px
- Body: Regular (400), 14-16px
- Labels: Semibold (600), 14px

### Components

#### Input Fields
- Border: 2px solid (gray)
- Focus: Border berubah ke primary color
- Background: Light gray saat normal
- Radius: 12px
- Padding: 12px 16px

```html
<x-text-input 
    class="input-field block mt-2 w-full px-4 py-3 
    text-gray-900 border-2 border-gray-300 rounded-lg focus:ring-0" 
/>
```

#### Buttons
- Primary Button: Gradient ungu
- Secondary Button: Gray dengan border
- Hover: Slight translate + shadow
- Active: Kembali ke posisi normal
- Radius: 12px

```html
<button class="btn-primary w-full px-4 py-3 
    bg-gradient-to-r from-purple-600 to-purple-700 
    text-white font-semibold rounded-lg">
    Masuk
</button>
```

#### Form Elements
- Error Messages: Red text dengan bullet point
- Success Messages: Green background dengan left border
- Links: Hover dengan color change smooth
- Checkboxes: Custom accent color (primary)

## 🚀 Features

✅ **Modern Design**
- Gradient background dengan dekoratif elements
- Shadow depth yang appropriate
- Smooth transitions & animations

✅ **User Experience**
- Clear form labels
- Helpful placeholder text
- Error messages yang jelas
- Password requirements
- Remember me & forgot password options

✅ **Responsive Design**
- Mobile-friendly layouts
- Touch-friendly button sizes
- Proper font sizing untuk iOS (prevent zoom)

✅ **Accessibility**
- Focus states untuk keyboard navigation
- Color contrast yang baik
- Semantic HTML structure
- ARIA attributes ready

## 📱 Responsive Breakpoints

```css
/* Desktop: Full width */
.auth-card { max-width: 28rem; }

/* Tablet & Mobile: Adjusted padding */
@media (max-width: 768px) {
    .auth-card { padding: 24px 20px; }
    .input-field { font-size: 16px; } /* Prevent zoom */
}
```

## 🎬 Animations

### Slide Up (Card Entry)
```css
@keyframes slideUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
```

### Button Hover
```css
.btn-primary:hover {
    transform: translateY(-2px);
    box-shadow: 0 10px 30px rgba(102, 126, 234, 0.3);
}
```

## 🔧 Customization

### Mengubah Warna Primary
Edit di `resources/views/layouts/guest.blade.php` dan `resources/css/auth.css`:

```css
--primary-color: #667eea;
--primary-dark: #764ba2;
```

### Mengubah Border Radius
```css
--border-radius: 12px; /* Ubah ke nilai yang diinginkan */
```

## ✨ Best Practices

1. **Consistency**: Gunakan color palette yang sama di seluruh app
2. **Spacing**: Gunakan unit yang konsisten (12px, 16px, 24px)
3. **Typography**: Max 3 font sizes untuk hierarchy
4. **Shadows**: Gunakan shadows untuk depth, bukan borders
5. **Animations**: Keep animations smooth (<300ms)

## 📦 File Structure

```
resources/
├── views/
│   ├── auth/
│   │   ├── login.blade.php (updated)
│   │   └── register.blade.php (updated)
│   ├── layouts/
│   │   └── guest.blade.php (updated)
│   └── components/
│       ├── auth-session-status.blade.php (updated)
│       └── input-error.blade.php (updated)
└── css/
    ├── app.css (updated - added auth.css import)
    └── auth.css (new)
```

## 🎓 Maintenance Notes

- CSS di-import via `resources/css/app.css`
- Semua styles menggunakan Tailwind + custom CSS
- Fonts dimuat dari Bunny Fonts (privacy-friendly)
- No external dependencies (pure CSS)

---

**Version**: 1.0  
**Last Updated**: May 2026  
**Author**: Design System Update
