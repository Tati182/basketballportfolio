import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Instagram, Mail } from "lucide-react";

const photos = [
  { src: "![IMG_3117]", alt: "Basketball action 1" },
  { src: "![IMG_1874]", alt: "Basketball action 2" },
  { src: "![IMG_1867]", alt: "Basketball action 3" },
];

export default function Portfolio() {
  return (
    <div className="min-h-screen bg-gradient-to-tr from-orange-200 to-yellow-100 p-8 font-sans">
      <header className="text-center mb-12">
        <h1 className="text-5xl font-bold text-orange-600">Tatiana's Sports Photography</h1>
        <p className="text-lg mt-2 text-orange-800">Specializing in basketball moments, captured with heart.</p>
      </header>

      <section className="grid md:grid-cols-3 gap-6 mb-16">
        {photos.map((photo, idx) => (
          <Card key={idx} className="rounded-2xl shadow-lg overflow-hidden">
            <img src={photo.src} alt={photo.alt} className="w-full h-64 object-cover" />
            <CardContent className="p-4">
              <p className="text-sm text-orange-700">{photo.alt}</p>
            </CardContent>
          </Card>
        ))}
      </section>

      <footer className="text-center mt-10">
        <p className="mb-4 text-orange-700">Get in touch or follow my work:</p>
        <div className="flex justify-center gap-4">
          <Button variant="outline" className="rounded-full border-orange-400 text-orange-700">
            <Instagram className="w-5 h-5 mr-2" /> Instagram
          </Button>
          <Button variant="outline" className="rounded-full border-orange-400 text-orange-700">
            <Mail className="w-5 h-5 mr-2" /> Email
          </Button>
        </div>
      </footer>
    </div>
  );
}
