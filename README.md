#============================================================================== 
# ■ Vocab 
#------------------------------------------------------------------------------ 
# 　用語とメッセージを定義するモジュールです。定数でメッセージなどを直接定義す 
# るほか、グローバル変数 $data_system から用語データを取得します。 
#============================================================================== 

module Vocab 

ShopBuy = "Comprar" 
ShopSell = "Vender" 
ShopCancel = "Salir" 
Possession = "En posesión" 

# ステータス画面 
ExpTotal = "Experiencia" 
ExpNext = "Siguiente Nivel: %s" 

# セーブ／ロード画面 
SaveMessage = "¿Dónde quieres Guardar?" 
LoadMessage = "¿Qué archivo quieres Cargar?" 
File = "Archivo" 

# 複数メンバーの場合の表示 
PartyName = "El grupo de %s" 

# 戦闘基本メッセージ 
Emerge = "¡Ha aparecido %s!" 
Preemptive = "¡Ataque preventivo!" 
Surprise = "¡Los enemigos toman la iniciativa!" 
EscapeStart = "%s huye." 
EscapeFailure = "...lamentablemente, los enemigos le barran el paso." 

# 戦闘終了メッセージ 
Victory = "¡Victoria! ¡Has ganado!" 
Defeat = "%s ha caído." 
ObtainExp = "¡%s Puntos de Experiencia obtenidos!" 
ObtainGold = "¡%s \G obtenidos!" 
ObtainItem = "¡%s obtenido!" 
LevelUp = "¡%s sube al %s %s!" 
ObtainSkill = "¡Habilidad %s aprendida!" 

# アイテム使用 
UseItem = "%s usa %s." 

# クリティカルヒット 
CriticalToEnemy = "¡Un golpe Crítico!" 
CriticalToActor = "¡Un impacto Fatal!" 

# アクター対象の行動結果 
ActorDamage = "¡%s pierde %s PV!" 
ActorRecovery = "¡%s recupera %s %s!" 
ActorGain = "¡%s ha ganado %s %s!" 
ActorLoss = "¡%s ha perdido %s %s!" 
ActorDrain = "¡%s pierde %s %s!" 
ActorNoDamage = "¡%s sale ileso!" 
ActorNoHit = "¡Impacto fallido! %s no sufre ningún daño." 

# 敵キャラ対象の行動結果 
EnemyDamage = "¡%s pierde %s PV!" 
EnemyRecovery = "¡%s sana %s %s!" 
EnemyGain = "¡%s gana %s %s!" 
EnemyLoss = "¡%s pierde %s %s!" 
EnemyDrain = "¡%s pierde %s %s!" 
EnemyNoDamage = "¡%s sale ileso!" 
EnemyNoHit = "¡Pero falló! ¡% sale ileso!" 

# 回避／反射 
Evasion = "¡%s evade el ataque!" 
MagicEvasion = "¡%s evita el conjuro!" 
MagicReflection = "¡%s devuelve el conjuro!" 
CounterAttack = "¡%s contraataca!" 
Substitute = "¡%s coloca un %s!" 

# 能力強化／弱体 
BuffAdd = "¡%s queda afectado por %s!" 
DebuffAdd = "¡%s queda afectado por %s!" 
BuffRemove = "¡%s se libera de %s!" 

# スキル、アイテムの効果がなかった 
ActionFailure = "%s no logra realizar la acción." 

# エラーメッセージ 
PlayerPosError = "Posición Inicial de Jugador no especificada." 
EventOverflow = "Límite de Llamada de Eventos superado." 


# 基本ステータス 
def self.basic(basic_id) 
$data_system.terms.basic[basic_id] 
end 

# 能力値 
def self.param(param_id) 
$data_system.terms.params[param_id] 
end 

# 装備タイプ 
def self.etype(etype_id) 
$data_system.terms.etypes[etype_id] 
end 

# コマンド 
def self.command(command_id) 
$data_system.terms.commands[command_id] 
end 

# 通貨単位 
def self.currency_unit 
$data_system.currency_unit 
end 

 #--------------------------------------------------------------------------
  def self.level;       basic(0);     end   # レベル
  def self.level_a;     basic(1);     end   # レベル (短)
  def self.hp;          basic(2);     end   # HP
  def self.hp_a;        basic(3);     end   # HP (短)
  def self.mp;          basic(4);     end   # MP
  def self.mp_a;        basic(5);     end   # MP (短)
  def self.tp;          basic(6);     end   # TP
  def self.tp_a;        basic(7);     end   # TP (短)
  def self.fight;       command(0);   end   # 戦う
  def self.escape;      command(1);   end   # 逃げる
  def self.attack;      command(2);   end   # 攻撃
  def self.guard;       command(3);   end   # 防御
  def self.item;        command(4);   end   # アイテム
  def self.skill;       command(5);   end   # スキル
  def self.equip;       command(6);   end   # 装備
  def self.status;      command(7);   end   # ステータス
  def self.formation;   command(8);   end   # 並び替え
  def self.save;        command(9);   end   # セーブ
  def self.game_end;    command(10);  end   # ゲーム終了
  def self.weapon;      command(12);  end   # 武器
  def self.armor;       command(13);  end   # 防具
  def self.key_item;    command(14);  end   # 大事なもの
  def self.equip2;      command(15);  end   # 装備変更
  def self.optimize;    command(16);  end   # 最強装備
  def self.clear;       command(17);  end   # 全て外す
  def self.new_game;    command(18);  end   # ニューゲーム
  def self.continue;    command(19);  end   # コンティニュー
  def self.shutdown;    command(20);  end   # シャットダウン
  def self.to_title;    command(21);  end   # タイトルへ
  def self.cancel;      command(22);  end   # やめる
  #--------------------------------------------------------------------------
end
