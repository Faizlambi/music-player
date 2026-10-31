from kivy.app import App
from kivy.uix.floatlayout import FloatLayout
from kivy.uix.image import Image
from kivy.uix.button import Button
from kivy.core.audio import SoundLoader

class MusicApp(App):
    def build(self):
        self.sound = None
        root = FloatLayout()

        # BACKGROUND - tinggal ganti file background.jpg di github
        self.bg = Image(source='background.jpg', allow_stretch=True, keep_ratio=False)
        root.add_widget(self.bg)

        # LOGO - tinggal ganti file logo.png di github
        self.logo = Image(source='logo.png', size_hint=(0.5, 0.5), pos_hint={'center_x':0.5, 'center_y':0.7})
        root.add_widget(self.logo)

        btn = Button(text='PLAY / STOP', size_hint=(0.8, 0.15), pos_hint={'center_x':0.5, 'y':0.1})
        btn.bind(on_press=self.play_music)
        root.add_widget(btn)
        return root

    def play_music(self, x):
        if not self.sound:
            self.sound = SoundLoader.load('lagu.mp3')
            self.sound.play()
        else:
            self.sound.stop()
            self.sound = None

MusicApp().run()
