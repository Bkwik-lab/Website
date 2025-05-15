# Website
Lol
import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; import { Mail, Phone } from "lucide-react"; import { motion } from "framer-motion";

export default function HomePage() { return ( <div className="min-h-screen bg-gradient-to-br from-gray-50 to-blue-100 p-8 text-gray-800"> <header className="text-center mb-12"> <h1 className="text-4xl font-bold mb-2">مرحبًا بك في موقعي الحديث</h1> <p className="text-lg">موقع بسيط واحترافي باستخدام React و Tailwind</p> </header>

<section className="grid md:grid-cols-3 gap-6 mb-12">
    <Card>
      <CardContent className="p-6 text-center">
        <motion.img
          src="https://cdn-icons-png.flaticon.com/512/3135/3135715.png"
          alt="فريق العمل"
          className="mx-auto mb-4 w-16 h-16"
          initial={{ scale: 0.8, opacity: 0 }}
          animate={{ scale: 1, opacity: 1 }}
          transition={{ duration: 0.6 }}
        />
        <h2 className="text-xl font-semibold mb-2">من نحن</h2>
        <p className="mb-4">
          نحن فريق شغوف بصناعة الويب، نؤمن بأن التصميم الجيد والتجربة السلسة هما أساس أي مشروع ناجح.
          نستخدم أحدث تقنيات الويب لبناء مواقع تواكب المستقبل وتلبي تطلعات عملائنا.
          نعمل بشغف، ونؤمن بالتفاصيل.
        </p>
        <Button variant="outline">اعرف المزيد</Button>
      </CardContent>
    </Card>

    <Card>
      <CardContent className="p-6">
        <Mail className="mb-4 w-8 h-8 text-green-500" />
        <h2 className="text-xl font-semibold mb-2">اشترك في النشرة</h2>
        <div className="space-y-2">
          <Input placeholder="بريدك الإلكتروني" className="w-full" />
          <Button className="w-full">اشترك</Button>
        </div>
      </CardContent>
    </Card>

    <Card>
      <CardContent className="p-6">
        <Phone className="mb-4 w-8 h-8 text-red-500" />
        <h2 className="text-xl font-semibold mb-2">تواصل معنا</h2>
        <p>راسلنا في أي وقت وسنعود إليك قريبًا. نحب أن نسمع منك!</p>
      </CardContent>
    </Card>
  </section>

  <footer className="text-center text-sm text-gray-500">
    &copy; {new Date().getFullYear()} موقع تجريبي. كل الحقوق محفوظة.
  </footer>
</div>

); }

