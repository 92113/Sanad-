import React from "react";

// SKH_JEWELRY - Single-file React component (TailwindCSS)
// Default export: Landing page + simple product grid + contact form
// Text is in Arabic and tailored to متجر S.KH JEWELRY

export default function SKHWebsite() {
  const products = [
    { id: 1, name: "طقم أنيق من الفضة", price: "35 USD", img: "https://via.placeholder.com/400x400?text=منتج+1" },
    { id: 2, name: "سوار بسيط", price: "18 USD", img: "https://via.placeholder.com/400x400?text=منتج+2" },
    { id: 3, name: "خاتم مميز", price: "22 USD", img: "https://via.placeholder.com/400x400?text=منتج+3" },
    { id: 4, name: "قلادة فضية", price: "28 USD", img: "https://via.placeholder.com/400x400?text=منتج+4" }
  ];

  return (
    <div className="min-h-screen bg-gray-50 text-gray-900">
      {/* NAV */}
      <header className="bg-white shadow">
        <div className="container mx-auto px-4 py-4 flex items-center justify-between">
          <div className="flex items-center gap-3">
            <div className="w-10 h-10 bg-gradient-to-br from-pink-500 to-yellow-300 rounded-full flex items-center justify-center text-white font-bold">S.K</div>
            <div>
              <h1 className="text-lg font-semibold">S.KH JEWELRY</h1>
              <p className="text-xs text-gray-500">مجوهرات وإكسسوارات أنيقة</p>
            </div>
          </div>
          <nav className="hidden md:flex gap-6 items-center">
            <a href="#products" className="hover:underline">المنتجات</a>
            <a href="#about" className="hover:underline">من نحن</a>
            <a href="#contact" className="hover:underline">اتصل بنا</a>
            <button className="bg-pink-500 text-white px-4 py-2 rounded-lg">سلة التسوق</button>
          </nav>
        </div>
      </header>

      {/* HERO */}
      <section className="container mx-auto px-4 py-12 flex flex-col md:flex-row items-center gap-8">
        <div className="flex-1">
          <h2 className="text-3xl md:text-4xl font-extrabold">طقم مجوهرات يجمع الأناقة والاقتصاد</h2>
          <p className="mt-4 text-gray-600">نقدم تشكيلة مختارة من القلائد، الأساور، والخواتم المصممة بعناية لتناسب كل الأذواق. اشترِ الآن وتمتع بشحن سريع وخدمة عملاء مميزة.</p>
          <div className="mt-6 flex gap-4">
            <a href="#products" className="px-5 py-3 bg-pink-500 text-white rounded-lg font-semibold">تسوق الآن</a>
            <a href="#contact" className="px-5 py-3 border rounded-lg">اطلب فاتورة</a>
          </div>

          <div className="mt-8 grid grid-cols-2 sm:grid-cols-3 gap-3">
            <div className="text-sm text-gray-700">✅ جودة مضمونة</div>
            <div className="text-sm text-gray-700">🚚 توصيل داخل ليبيا</div>
            <div className="text-sm text-gray-700">💬 دعم سريع عبر الواتساب</div>
          </div>
        </div>

        <div className="flex-1">
          <img src="https://via.placeholder.com/600x400?text=SKH+JEWELRY" alt="hero" className="w-full rounded-xl shadow" />
        </div>
      </section>

      {/* PRODUCTS */}
      <section id="products" className="container mx-auto px-4 py-10">
        <h3 className="text-2xl font-bold mb-6">منتجات مميزة</h3>
        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
          {products.map(p => (
            <article key={p.id} className="bg-white rounded-xl shadow p-4 flex flex-col">
              <img src={p.img} alt={p.name} className="w-full h-48 object-cover rounded-md" />
              <h4 className="mt-3 font-semibold">{p.name}</h4>
              <p className="text-pink-600 mt-1 font-bold">{p.price}</p>
              <div className="mt-auto pt-4 flex gap-2">
                <button className="flex-1 px-3 py-2 bg-pink-500 text-white rounded-md">اضف الى السلة</button>
                <button className="px-3 py-2 border rounded-md">معاينة</button>
              </div>
            </article>
          ))}
        </div>
      </section>

      {/* ABOUT */}
      <section id="about" className="container mx-auto px-4 py-12">
        <div className="bg-white rounded-xl shadow p-6 md:flex gap-6">
          <div className="md:w-1/2">
            <h3 className="text-2xl font-bold">من نحن</h3>
            <p className="mt-3 text-gray-600">متجر S.KH JEWELRY متخصص في بيع مجوهرات وإكسسوارات صغيرة ومحلية الصنع، تأسس ليقدم قطعاً ذات جودة وتصميم عصري. نعمل على تلبية طلبات العملاء سواءً بالجملة أو التجزئة.</p>
            <ul className="mt-4 space-y-2 text-gray-700">
              <li>• شحن داخل ليبيا</li>
              <li>• طلبات خاصة وتصميم حسب الطلب</li>
              <li>• دعم واستبدال خلال 7 أيام</li>
            </ul>
          </div>
          <div className="md:w-1/2 mt-6 md:mt-0">
            <h4 className="font-semibold">نماذج أعمال سابقة</h4>
            <div className="grid grid-cols-2 gap-3 mt-3">
              <img src="https://via.placeholder.com/200?text=نماذج" alt="نماذج" className="rounded-md" />
              <img src="https://via.placeholder.com/200?text=نماذج" alt="نماذج" className="rounded-md" />
            </div>
          </div>
        </div>
      </section>

      {/* CONTACT */}
      <section id="contact" className="container mx-auto px-4 py-12">
        <div className="bg-white rounded-xl shadow p-6 md:flex gap-6">
          <div className="md:w-1/2">
            <h3 className="text-2xl font-bold">اتصل بنا</h3>
            <p className="mt-2 text-gray-600">للطلبات أو الاستفسار حول المنتجات راسلنا عبر الواتساب أو املأ النموذج.</p>

            <div className="mt-4 space-y-3 text-gray-700">
              <div>📞 الهاتف: 218921136769+</div>
              <div>📧 البريد: Sanadkh04@gmail.com</div>
              <div>📍 الموقع: جنزور، ليبيا</div>
            </div>
          </div>

          <form className="md:w-1/2 mt-6 md:mt-0 space-y-3">
            <input className="w-full border rounded-md p-2" placeholder="اسمك" />
            <input className="w-full border rounded-md p-2" placeholder="البريد الإلكتروني" />
            <textarea className="w-full border rounded-md p-2" rows={4} placeholder="رسالتك / طلب المنتج"></textarea>
            <div className="flex gap-3">
              <button type="button" className="px-4 py-2 bg-pink-500 text-white rounded-md">أرسل</button>
              <button type="reset" className="px-4 py-2 border rounded-md">مسح</button>
            </div>
          </form>
        </div>
      </section>

      {/* FOOTER */}
      <footer className="bg-white mt-12">
        <div className="container mx-auto px-4 py-6 flex flex-col md:flex-row justify-between items-center">
          <p className="text-sm text-gray-600">© {new Date().getFullYear()} S.KH JEWELRY. جميع الحقوق محفوظة.</p>
          <div className="flex gap-3 mt-3 md:mt-0">
            <a className="text-sm hover:underline">سياسة الخصوصية</a>
            <a className="text-sm hover:underline">الشحن والإرجاع</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
