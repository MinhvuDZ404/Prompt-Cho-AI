# MASTER PROMPT

# XÂY DỰNG GAME WEB VOXEL 3D SANDBOX QUY MÔ LỚN

# MỤC TIÊU TRẢI NGHIỆM TƯƠNG ĐỒNG RẤT CAO VỚI DÒNG GAME MINECRAFT

# NHƯNG TOÀN BỘ MÃ NGUỒN, ASSET, TÊN GỌI, ÂM THANH VÀ NỘI DUNG PHẢI NGUYÊN BẢN

---

## 0. VAI TRÒ CỦA BẠN

Bạn không chỉ là một lập trình viên.

Trong dự án này, bạn phải đồng thời hoạt động như:

* Game Director.
* Lead Game Designer.
* Senior TypeScript Engineer.
* Senior WebGL/WebGPU Engineer.
* Voxel Engine Engineer.
* Gameplay Programmer.
* Physics Programmer.
* AI Programmer.
* UI/UX Designer.
* Technical Artist.
* Audio Designer.
* Performance Engineer.
* QA Lead.
* Automation Test Engineer.
* Save-System Architect.
* Systems Designer.
* Debugging Engineer.
* Security Engineer ở mức phù hợp với game web.
* Release Engineer.
* Product Owner.
* Technical Writer.

Hãy tự đưa ra các quyết định kỹ thuật cần thiết.

Không được hiểu prompt này như một checklist cứng khiến bạn chỉ làm đúng từng dòng rồi dừng lại.

Mục tiêu thực sự là tạo ra một game web voxel sandbox hoàn chỉnh, sâu, mượt, ổn định, hấp dẫn, có khả năng chơi lâu dài và có trải nghiệm tổng thể gần với một game Minecraft-style hiện đại.

Nếu trong quá trình triển khai bạn phát hiện một hệ thống quan trọng đang thiếu, một lỗi kiến trúc có nguy cơ gây ra lỗi về sau, hoặc một cơ chế cần được bổ sung để game hoàn chỉnh hơn, hãy chủ động thiết kế và triển khai nó.

Không chờ người dùng phải chỉ từng bước.

Không chỉ sửa lỗi bề mặt.

Không chỉ làm cho demo chạy được.

Không chỉ làm game “trông giống game”.

Bạn phải xây dựng một sản phẩm có kiến trúc thực sự.

---

# 1. MỤC TIÊU TỔNG THỂ

Hãy xây dựng một game web 3D voxel sandbox quy mô lớn, chạy trực tiếp trên trình duyệt, với cảm giác chơi rất gần các game sandbox voxel nổi tiếng, đặc biệt là Minecraft, xét trên các nhóm trải nghiệm sau:

* thế giới voxel.
* khám phá tự do.
* phá block.
* đặt block.
* thu thập tài nguyên.
* crafting.
* inventory.
* công cụ.
* chiến đấu.
* sinh vật.
* ngày và đêm.
* môi trường.
* hang động.
* quặng.
* cây cối.
* biome.
* thời tiết.
* sinh tồn.
* xây dựng.
* khám phá.
* tiến trình.
* thế giới được sinh procedural.
* seed.
* lưu game.
* tải game.
* chunk streaming.
* thế giới rất lớn.
* gameplay sandbox.
* tương tác vật lý.
* âm thanh môi trường.
* hiệu ứng hình ảnh.
* UI.
* camera góc nhìn thứ nhất.
* phản hồi thao tác.
* hệ thống tài nguyên.
* NPC.
* nhiệm vụ hoặc mục tiêu dài hạn.
* progression.
* hệ thống chiến đấu.
* enemy AI.
* boss hoặc thực thể đặc biệt.
* các hệ thống automation hoặc contraption ở mức phù hợp.
* khả năng chơi trong thời gian dài mà không cảm thấy chỉ là một prototype.

Mục tiêu “giống Minecraft khoảng 90%” ở đây phải được hiểu là:

> Đạt mức tương đồng rất cao về cảm giác của một game voxel sandbox, cấu trúc vòng lặp gameplay, độ sâu hệ thống, cách người chơi khám phá thế giới, khai thác, xây dựng, chế tạo, sinh tồn và chiến đấu.

Không được sao chép:

* logo Minecraft.
* tên Minecraft.
* tên Mojang.
* texture gốc.
* model gốc.
* sound effect gốc.
* music gốc.
* font độc quyền.
* UI artwork gốc.
* mã nguồn gốc.
* world seed gốc.
* nhân vật độc quyền.
* asset thương mại có bản quyền.
* nội dung nguyên xi.
* ảnh chụp hoặc sprite lấy trực tiếp từ game.

Hãy xây một sản phẩm có DNA gameplay tương đồng nhưng có bản sắc riêng.

---

# 2. NGUYÊN TẮC ƯU TIÊN

Khi phải lựa chọn giữa nhiều giải pháp, ưu tiên theo thứ tự:

1. Tính ổn định.
2. Tính chính xác logic.
3. Tính nhất quán trạng thái.
4. Khả năng chơi thật.
5. Hiệu năng.
6. Khả năng mở rộng.
7. UX.
8. Visual quality.
9. Audio quality.
10. Tính thuận tiện cho việc phát triển tiếp.

Không được hy sinh kiến trúc ổn định chỉ để tạo một hiệu ứng đẹp.

Không được hy sinh gameplay chỉ để đạt FPS cao.

Không được hy sinh tính đúng đắn của save system để demo chạy nhanh.

Không được tạo hack tạm thời chỉ để vượt qua test.

Mọi workaround phải có lý do kỹ thuật rõ ràng và không được tạo debt nghiêm trọng.

---

# 3. NGUYÊN TẮC TỰ CHỦ

Bạn được toàn quyền đưa ra quyết định triển khai nếu quyết định đó:

* giúp game hoàn chỉnh hơn;
* giúp hệ thống ổn định hơn;
* cải thiện performance;
* cải thiện UX;
* giảm bug;
* làm gameplay hấp dẫn hơn;
* làm kiến trúc sạch hơn;
* giúp game dễ mở rộng.

Bạn không cần hỏi lại người dùng cho các quyết định nhỏ.

Bạn phải tự nhận diện:

* missing systems;
* architectural risks;
* inconsistent naming;
* duplicated logic;
* stale state;
* race conditions;
* memory leaks;
* physics bugs;
* rendering bugs;
* save corruption risks;
* UI state bugs;
* performance regressions;
* asset loading failures.

Nếu một phần hiện tại chưa đủ để hỗ trợ mục tiêu cuối cùng, hãy xây lại phần đó một cách hợp lý.

---

# 4. KHÔNG ĐƯỢC DỪNG Ở PROTOTYPE

Tôi không cần:

* một demo đẹp nhưng gameplay rỗng;
* một terrain đẹp nhưng không có progression;
* một character di chuyển được nhưng physics lỗi;
* một inventory có giao diện nhưng không đồng bộ state;
* một crafting panel không hoạt động;
* một world generator chỉ tạo vài chunk;
* một game nhìn giống voxel nhưng không thể chơi hàng giờ.

Tôi cần một game thật sự có vòng lặp:

KHÁM PHÁ → THU THẬP → CHẾ TẠO → XÂY DỰNG → NÂNG CẤP → CHIẾN ĐẤU → KHÁM PHÁ SÂU HƠN → THU THẬP TÀI NGUYÊN HIẾM → MỞ KHÓA KHẢ NĂNG MỚI → TIẾP TỤC XÂY DỰNG VÀ KHÁM PHÁ.

Vòng lặp này phải có chiều sâu.

---

# 5. NỀN TẢNG CÔNG NGHỆ

Ưu tiên sử dụng:

* TypeScript.
* Vite hoặc toolchain tương đương.
* Three.js hoặc engine WebGL/WebGPU phù hợp.
* WebGL2 làm nền tảng tương thích chính.
* WebGPU có thể được hỗ trợ như renderer nâng cao nếu kiến trúc cho phép.
* IndexedDB cho persistent world data.
* localStorage cho cấu hình nhỏ và backup metadata.
* Web Workers cho tác vụ nặng.
* requestAnimationFrame.
* object pooling.
* chunk streaming.
* mesh batching.
* greedy meshing hoặc kỹ thuật culling tương đương.
* texture atlas.
* typed arrays khi phù hợp.
* deterministic procedural generation.

Không được dùng công nghệ chỉ vì “trông hiện đại”.

Mọi lựa chọn phải phục vụ:

* độ ổn định;
* hiệu năng;
* maintainability;
* khả năng debug;
* tương thích trình duyệt.

Nếu có thể thiết kế hệ thống renderer để hỗ trợ nhiều backend mà không làm kiến trúc quá phức tạp, hãy làm.

---

# 6. KIẾN TRÚC CODE

Không được biến toàn bộ project thành một file khổng lồ.

Không được tạo:

* một Game.ts dài hàng chục nghìn dòng;
* một Player class làm mọi thứ;
* một global state hỗn loạn;
* các singleton phụ thuộc vòng tròn;
* các module có trách nhiệm chồng chéo.

Tách rõ các lớp hệ thống.

Ví dụ:

core/

engine/

world/

chunks/

terrain/

blocks/

items/

inventory/

crafting/

entities/

player/

physics/

combat/

ai/

rendering/

lighting/

particles/

audio/

ui/

input/

save/

settings/

events/

testing/

workers/

assets/

scenes/

debug/

analytics/

constants/

data/

recipes/

biomes/

structures/

weather/

quests/

progression/

Mỗi module phải có trách nhiệm rõ ràng.

Không tạo abstraction vô nghĩa.

Không tạo hệ thống quá phức tạp khi một abstraction đơn giản đã đủ.

---

# 7. SINGLE SOURCE OF TRUTH

Mọi trạng thái quan trọng phải có nguồn dữ liệu chuẩn.

Ví dụ:

* inventory;
* player health;
* player hunger;
* equipment;
* world time;
* chunk state;
* block state;
* entity state;
* weather;
* seed;
* progression;
* unlocked recipes;
* world metadata.

Không được để:

UI state ≠ game state.

Render state ≠ authoritative gameplay state.

Save state ≠ runtime state.

Trừ khi sự tách biệt đó có chủ đích.

Mọi chuyển đổi phải rõ ràng.

---

# 8. DATA-DRIVEN DESIGN

Block không được hardcode trong hàng trăm if/else.

Item không được hardcode tương tự.

Recipe không được trải khắp game code.

Mob stats không được rải khắp AI.

Biomes không được viết trực tiếp trong terrain generator.

Hãy dùng data-driven configuration.

Mỗi block có thể có:

* id;
* name;
* hardness;
* requiredTool;
* drops;
* texture;
* collision;
* transparency;
* emission;
* friction;
* soundGroup;
* tags;
* materialGroup.

Item có:

* id;
* category;
* stackSize;
* rarity;
* durability;
* icon;
* useAction;
* tags.

Entity có:

* id;
* type;
* health;
* movementSpeed;
* damage;
* armor;
* behavior;
* drops;
* spawnRules.

---

# 9. THẾ GIỚI VOXEL

World phải dựa trên grid voxel rõ ràng.

Mỗi block chiếm một cell.

World phải hỗ trợ:

* tọa độ world;
* tọa độ chunk;
* tọa độ local block;
* block lookup;
* block mutation;
* chunk boundaries;
* streaming.

Phải có utility chuyển đổi:

worldToChunk()

blockToChunk()

worldToLocal()

chunkToWorld()

localIndex()

và ngược lại.

Kiểm tra cực kỳ kỹ:

* coordinate âm;
* coordinate sát biên;
* tọa độ lớn;
* chunk âm;
* chunk transition;
* world origin;
* floating-point drift.

Không được có tình huống:

block ở chunk A được đọc thành block ở chunk B.

---

# 10. CHUNK SYSTEM

Chunk là đơn vị chính của world streaming.

Chunk cần:

* coordinates;
* blocks;
* metadata;
* generated state;
* loaded state;
* meshed state;
* dirty flag;
* save state;
* entity references phù hợp.

Chunk lifecycle:

UNLOADED

→ REQUESTED

→ GENERATING

→ GENERATED

→ MESHING

→ MESHED

→ ACTIVE

→ DIRTY

→ SAVING

→ SAVED

→ UNLOADED

Các transition phải hợp lệ.

Không được:

ACTIVE → UNLOADED trong khi hệ thống vẫn đang dùng references cũ.

Không được unload chunk vẫn chứa entity quan trọng nếu entity chưa được serialize.

Không được tạo nhiều generation job cùng lúc cho cùng một chunk mà không có cơ chế chống trùng.

---

# 11. CHUNK STREAMING

Camera/player di chuyển.

Hệ thống phải tự:

* load chunk gần;
* unload chunk xa;
* preload chunk phía trước hướng di chuyển;
* giữ vùng an toàn quanh player.

Streaming không được gây:

* freeze màn hình;
* teleport;
* mất block;
* chunk pop quá nghiêm trọng;
* mesh sai;
* entity duplication.

Nếu chunk đang generate ở worker và player rời vùng đó:

worker result vẫn phải được kiểm tra generation token.

Một kết quả cũ không được overwrite state mới.

Đây là một lớp lỗi concurrency cực kỳ quan trọng.

---

# 12. TERRAIN GENERATION

World phải được procedural.

Input chính:

* seed;
* world coordinate;
* world settings.

Kết quả cần deterministic.

Cùng seed + cùng version generator + cùng tọa độ:

→ cùng terrain.

Không dùng randomness toàn cục không kiểm soát.

Không được để thứ tự load chunk ảnh hưởng terrain.

Không được để FPS ảnh hưởng generation.

Không để async scheduling thay đổi kết quả.

---

# 13. ĐỊA HÌNH

Terrain nên có nhiều tầng:

* bedrock;
* stone;
* soil;
* grass;
* sand;
* snow;
* ore layers;
* underground structures.

Tạo:

* núi;
* đồi;
* đồng bằng;
* thung lũng;
* sông;
* hồ;
* biển;
* bờ biển;
* hang;
* vực;
* plateau;
* biome transitions.

Không làm terrain chỉ bằng một noise.

Kết hợp nhiều lớp noise:

height noise;

detail noise;

erosion-like noise;

temperature;

humidity;

continentalness;

cave noise;

ore noise;

structure noise.

Không cần copy thuật toán cụ thể từ Minecraft.

Hãy tạo thuật toán riêng có chất lượng tương đương về kết quả trải nghiệm.

---

# 14. BIOME SYSTEM

Tạo nhiều biome.

Ví dụ:

* Meadow.
* Forest.
* Dense Forest.
* Pine Forest.
* Desert.
* Badlands.
* Snowfield.
* Frozen Forest.
* Swamp.
* Savannah.
* Highlands.
* Rocky Mountains.
* Coastal.
* Deep Caverns.
* Mushroom Caverns.
* Crystal Caverns.
* Ashlands.
* Ancient Ruins biome.

Tên và artwork có thể sáng tạo.

Mỗi biome có:

* terrain profile;
* surface blocks;
* vegetation;
* mob spawn;
* climate;
* weather;
* particles;
* ambient audio;
* structures;
* resources.

Biome transition phải mượt.

Không để terrain đổi đột ngột thành một bức tường vô lý.

---

# 15. CAVE SYSTEM

Hang động phải thực sự có cảm giác khám phá.

Không chỉ là những khối rỗng ngẫu nhiên.

Tạo:

* narrow tunnels;
* large chambers;
* vertical shafts;
* underground lakes;
* underground rivers;
* branching systems;
* rare crystal areas;
* dangerous depths;
* ore pockets;
* hidden rooms;
* ruins.

Đảm bảo:

* không sinh cave làm cắt toàn bộ terrain ngoài ý muốn;
* không tạo hố không thể đi qua tại spawn nếu không chủ ý;
* không làm player sinh ra trong block;
* không tạo cấu trúc làm game crash.

---

# 16. ORE SYSTEM

Quặng phải có distribution hợp lý.

Mỗi ore có:

* minimum depth;
* maximum depth;
* frequency;
* cluster size;
* biome modifier;
* rarity.

Ví dụ tài nguyên nguyên bản:

* Copperite.
* Ironite.
* Ember Ore.
* Azure Crystal.
* Shadow Ore.
* Sunstone.
* Moon Crystal.
* Ancient Core.

Không cần dùng đúng tên tài nguyên Minecraft.

Mục tiêu là tạo progression tương tự:

common resource → improved tools → rare materials → endgame materials.

---

# 17. TREES AND VEGETATION

Thế giới không được cảm giác trống.

Tạo:

* cây;
* bụi;
* cỏ;
* hoa;
* nấm;
* cây khô;
* đá;
* cây đặc biệt;
* vegetation clusters.

Tree generator phải deterministic theo vị trí.

Không sinh cây đè vào player hoặc spawn structure.

Tránh tree overlap vô lý.

Hãy tạo nhiều biến thể cùng loài.

---

# 18. STRUCTURE GENERATION

Thêm structure procedural.

Ví dụ:

* abandoned cabin;
* ruins;
* watchtower;
* underground shrine;
* desert temple-style ruin nhưng có thiết kế riêng;
* frozen outpost;
* cave camp;
* ancient gate;
* dungeon room;
* mine;
* village-like settlement.

Mỗi structure có:

* footprint;
* anchor;
* orientation;
* loot;
* spawn rules;
* integrity.

Phải chống structure overlap hoặc cho phép overlap có chủ đích.

---

# 19. SPAWN SYSTEM

Player spawn phải an toàn.

Không spawn:

* trong nước sâu;
* trong lava;
* trong block;
* trên không;
* giữa hostile mob đông;
* ở vị trí không đứng được.

Có thể tìm safe spawn bằng:

1. terrain query;
2. collision test;
3. exposure test;
4. light/environment test;
5. fallback search.

Không bao giờ giả định vị trí spawn mặc định là hợp lệ.

---

# 20. PLAYER CONTROLLER

Player controller phải có:

* walking;
* running/sprinting;
* jumping;
* falling;
* gravity;
* collision;
* crouching hoặc alternate movement;
* swimming;
* climbing nếu có;
* head/body separation;
* camera-relative movement.

Mouse:

* nhìn;
* quay camera.

Keyboard:

* movement;
* jump;
* inventory;
* interaction;
* hotbar;
* sprint.

Touch:

* virtual movement;
* look;
* jump;
* interact;
* inventory.

Không được để input state bị “kẹt”.

Ví dụ:

keydown(W)

blur tab

keyup(W) không bao giờ xảy ra

→ player vẫn chạy mãi.

Phải xử lý:

window blur;

visibilitychange;

pointer lock loss;

touchcancel;

touchend;

gamepad disconnect.

---

# 21. CAMERA

Camera phải ổn định.

Không để:

* jitter;
* clipping;
* camera xuyên terrain;
* FOV thay đổi bất thường;
* mouse sensitivity mất đồng bộ;
* camera reset vô cớ.

Hỗ trợ:

* FOV;
* sensitivity;
* invert Y;
* render distance;
* head bob optional;
* view bob optional;
* camera smoothing optional.

Mọi option phải thực sự tác động đúng vào game.

---

# 22. PHYSICS

Physics không cần quá phức tạp nhưng phải đáng tin cậy.

Cần:

* AABB collision;
* gravity;
* step handling;
* slope handling nếu có;
* terminal velocity;
* grounded state;
* wall collision;
* ceiling collision;
* falling damage;
* water movement.

Đặc biệt kiểm tra:

fast player + thin wall;

fast falling;

small ledge;

corner collision;

diagonal movement;

jump while moving;

movement across chunk border.

Phải chống tunneling ở mức phù hợp.

---

# 23. BLOCK INTERACTION

Player phải có raycast.

Raycast phải xác định:

* block hit;
* face hit;
* hit position;
* distance;
* placement position.

Phải xử lý:

* phá block;
* đặt block;
* interaction block;
* inaccessible block;
* reach distance.

Không cho phép đặt block tại vị trí làm player bị kẹt trong collision.

Sau block mutation:

* update chunk;
* mark dirty;
* update neighboring chunk mesh khi cần;
* update collision;
* update lighting;
* update save state.

---

# 24. MINING

Mining phải có cảm giác tốt.

Bao gồm:

* progress;
* hardness;
* tool modifier;
* damage animation;
* particles;
* block break sound;
* item drop;
* tool wear.

Không để:

* double drops;
* zero drops do race;
* block visual biến mất nhưng collision vẫn còn;
* collision biến mất nhưng visual vẫn còn.

Block destruction phải là một transaction logic nhất quán.

---

# 25. BLOCK PLACEMENT

Placement:

* preview;
* grid snapping;
* face orientation;
* valid placement;
* invalid placement feedback;
* inventory consumption;
* block update.

Transaction:

validate

→ reserve/check item

→ place

→ update world

→ consume item

→ update save state

Nếu bước nào thất bại:

rollback.

Không được:

* mất item nhưng block không đặt;
* đặt block nhưng item không trừ;
* double placement.

---

# 26. INVENTORY

Inventory phải là hệ thống thật.

Có:

* slots;
* stack;
* split;
* merge;
* swap;
* drag;
* quick move;
* hotbar;
* equipment;
* item metadata.

Invariant quan trọng:

Không được âm số lượng item.

Không được tạo item miễn phí do race condition.

Không được nhân đôi item do drag/drop.

Không được mất item do UI reopen.

Mọi inventory mutation phải thông qua một API trung tâm.

---

# 27. ITEM STACKING

Stacking logic phải deterministic.

Hai item chỉ stack nếu:

* cùng item ID;
* metadata tương thích;
* durability tương thích nếu cần;
* variant tương thích.

Nếu item khác metadata:

không được merge sai.

---

# 28. HOTBAR

Hotbar phải:

* chọn slot;
* wheel scroll;
* number keys;
* touch friendly;
* visual feedback.

Hotbar phải phản ánh inventory thật.

Không được tạo một hotbar copy độc lập có state riêng.

Hotbar chỉ là một view/controller trên inventory state.

---

# 29. CRAFTING

Crafting phải data-driven.

Recipe có:

* id;
* pattern;
* ingredients;
* output;
* quantity;
* unlock condition;
* station requirement.

Hỗ trợ:

* crafting grid;
* quick craft;
* recipe search;
* filtering;
* category;
* locked recipes;
* required materials.

Không được để UI cho phép craft nếu backend logic không cho phép.

---

# 30. CRAFTING TRANSACTIONS

Mỗi craft operation là transaction:

CHECK

→ RESERVE

→ CONSUME

→ CREATE

→ COMMIT.

Nếu lỗi:

→ ROLLBACK.

Không được xảy ra:

* consume nhưng không create output;
* create output mà không consume input;
* double craft;
* duplicate output.

---

# 31. TOOLS

Tạo nhiều tool tier.

Ví dụ:

* wooden-like;
* stone-like;
* metal;
* reinforced;
* crystal;
* ancient.

Nhưng dùng tên nguyên bản.

Tool có:

* mining speed;
* durability;
* damage;
* special effects;
* tags;
* preferred block class.

Tool phải ảnh hưởng thực sự đến gameplay.

---

# 32. DURABILITY

Durability phải:

* hiển thị;
* giảm đúng;
* không âm;
* không reset sau reload;
* không tăng vô cớ.

Nếu tool đạt 0:

* break;
* remove hoặc chuyển trạng thái unusable;
* feedback.

Test durability ở:

1;
2;
max;
0;
overflow.

---

# 33. COMBAT

Combat phải tạo cảm giác tốt.

Player có:

* attack;
* attack cooldown;
* hit detection;
* damage;
* knockback;
* critical hoặc special hit tùy thiết kế;
* weapon/tool differences.

Enemy có:

* health;
* armor;
* resistances;
* movement;
* attack;
* cooldown;
* death;
* loot.

Hit detection phải tránh:

* double hit;
* hit xuyên tường không hợp lệ;
* damage nhiều lần trong một frame ngoài ý muốn.

---

# 34. ENTITY SYSTEM

Không tạo một class duy nhất cho mọi entity.

Có:

BaseEntity

→ LivingEntity

→ Player

→ Mob

→ PassiveMob

→ HostileMob

→ Boss

hoặc kiến trúc ECS nếu phù hợp.

Entity phải có lifecycle:

spawned;

active;

sleeping;

dead;

despawned;

serialized.

Không được có entity “ma” vẫn được update sau khi remove.

---

# 35. MOB AI

AI phải thực sự có behavior.

Passive mobs:

* wander;
* idle;
* flee;
* seek food;
* follow;
* react.

Hostile mobs:

* detect;
* chase;
* navigate;
* attack;
* retreat;
* lose target;
* search target;
* avoid obstacles.

AI phải không block main thread khi có thể tránh.

Không để 500 entity gọi heavy pathfinding mỗi frame.

---

# 36. PATHFINDING

AI navigation phải có giới hạn.

Không chạy tìm đường vô hạn.

Mọi pathfinding job có:

* timeout;
* max nodes;
* cancel support;
* fallback behavior.

Nếu pathfinding thất bại:

mob phải quay về behavior an toàn.

Không được đứng im vĩnh viễn không lý do.

---

# 37. DAY/NIGHT CYCLE

World có thời gian liên tục.

Thời gian phải deterministic nếu cần.

Day cycle ảnh hưởng:

* sky;
* light;
* mob spawn;
* ambience;
* weather;
* NPC behavior;
* crops;
* world mood.

Không để thời gian reset khi reload.

Save:

worldTime

phải được lưu chính xác.

---

# 38. LIGHTING

Lighting là hệ thống quan trọng.

Hỗ trợ:

* sunlight;
* block light;
* emissive blocks;
* torch-like sources;
* ambient light.

Không nhất thiết phải sao chép lighting engine của Minecraft.

Nhưng phải tạo được:

* vùng sáng;
* vùng tối;
* chuyển tiếp tự nhiên;
* emissive material;
* cave ambience.

Khi phá/đặt source:

lighting update đúng.

Không được để light stale sau block mutation.

---

# 39. WATER

Nếu game hỗ trợ chất lỏng, hãy làm hệ thống đúng.

Water phải có:

* source;
* spread;
* level;
* flow;
* interaction.

Không được để fluid simulation tràn vô hạn không kiểm soát.

Có giới hạn update và chunk awareness.

Fluid có thể dùng simplified simulation nhằm đảm bảo performance.

---

# 40. LAVA / HAZARDOUS FLUID

Có thể thêm loại fluid nguy hiểm nguyên bản.

Tính chất:

* damage;
* heat;
* movement;
* light;
* interaction với blocks.

Không tạo simulation vô hạn.

---

# 41. WEATHER

Có:

* clear;
* rain;
* storm;
* snow-like weather;
* fog;
* wind.

Weather ảnh hưởng:

* lighting;
* particles;
* audio;
* ambience;
* mob behavior nếu phù hợp.

Không spam hàng nghìn DOM element.

Particle phải render bằng renderer, không phải DOM.

---

# 42. PARTICLES

Particle system phải pooling.

Không:

new particle

new particle

new particle

mỗi frame vô hạn.

Dùng object pool.

Particle types:

* block break;
* dust;
* smoke;
* sparks;
* hit;
* fire;
* water splash;
* snow;
* leaves;
* magic;
* ambient.

Có limit.

Nếu limit đạt max:

reuse hoặc discard.

Không crash.

---

# 43. VISUAL STYLE

Phong cách:

* voxel;
* stylized;
* sạch;
* dễ đọc;
* màu có chủ đích;
* silhouette rõ;
* lighting đẹp;
* texture nhất quán.

Không dùng:

* asset ngẫu nhiên không đồng bộ;
* emoji làm texture chính;
* placeholder ô vuông;
* icon hệ điều hành;
* hình ảnh lấy trực tiếp từ Minecraft.

Game phải có bản sắc riêng.

---

# 44. TEXTURE SYSTEM

Texture atlas.

Texture dimensions hợp lý.

Không tải hàng nghìn file nhỏ nếu không cần.

Support:

* top;
* bottom;
* side;
* overlay;
* emissive;
* transparent.

Atlas generation phải tránh:

* bleeding;
* UV seam;
* incorrect mipmaps;
* wrong face assignment.

---

# 45. RENDERING

Renderer phải tối ưu.

Ưu tiên:

* visible faces only;
* chunk mesh batching;
* frustum culling;
* distance culling;
* mesh reuse;
* texture atlas;
* object pooling.

Không render từng block như một Mesh riêng.

Nếu mỗi block là một object 3D riêng:

đó là dấu hiệu kiến trúc có vấn đề.

---

# 46. GREEDY MESHING

Nếu sử dụng greedy meshing:

hãy kiểm tra cực kỳ kỹ:

* face merging;
* normals;
* UVs;
* texture IDs;
* transparency;
* light data;
* chunk borders.

Đặc biệt:

chunk A phải render đúng mặt tiếp giáp chunk B.

Không có cracks.

Không có invisible walls.

Không có floating faces.

---

# 47. TRANSPARENT BLOCKS

Transparent materials phải có render order phù hợp.

Kiểm tra:

* glass-like blocks;
* water;
* leaves;
* translucent effects.

Không được tạo sorting bug rõ ràng.

---

# 48. SHADOWS

Nếu có dynamic shadows:

phải cân nhắc performance.

Không hy sinh FPS quá mạnh.

Có thể dùng:

* cascaded-like approximation;
* baked/cheap ambient;
* shadow distance;
* optional quality levels.

Quality setting phải thực sự thay đổi workload.

---

# 49. GRAPHICS SETTINGS

Có:

Low

Medium

High

Ultra

hoặc Auto.

Settings:

* render distance;
* shadows;
* particles;
* effects;
* anti-aliasing;
* resolution scale;
* post-processing;
* view distance;
* lighting quality.

Auto mode có thể theo:

FPS sampling.

Nhưng Auto không được thay đổi setting liên tục gây khó chịu.

---

# 50. FPS STABILITY

Không chỉ đo FPS trung bình.

Theo dõi:

* frame time;
* p50;
* p95;
* p99;
* stutter events;
* GC spikes.

Một game 60 FPS trung bình nhưng cứ vài giây freeze 300 ms vẫn là game có vấn đề.

Phải kiểm tra frame pacing.

---

# 51. MEMORY

Theo dõi:

* JS heap;
* GPU resource growth nếu có thể;
* textures;
* geometries;
* workers;
* event listeners.

Kiểm tra memory leak sau:

* mở game;
* đi xa;
* quay lại;
* load nhiều chunk;
* unload chunk;
* open/close menus;
* change settings;
* reload world;
* restart game.

Memory phải không tăng vô hạn theo thời gian.

---

# 52. WORKERS

Worker architecture phải an toàn.

Mỗi job cần:

* request ID;
* type;
* payload;
* result;
* cancellation hoặc stale-result handling.

Không để worker cũ ghi đè dữ liệu mới.

Worker error phải được bắt.

Worker termination phải sạch.

Nếu worker crash:

game phải có fallback hoặc thông báo rõ ràng, không silent corruption.

---

# 53. SAVE SYSTEM

Save system cực kỳ quan trọng.

Game không được chỉ save một JSON khổng lồ.

Thiết kế save layer hợp lý.

Có thể chia:

world metadata;

player;

inventory;

chunks;

entities;

progression;

settings.

Sử dụng IndexedDB.

Có version.

Ví dụ:

schemaVersion: 1

khi update:

1 → 2

2 → 3

Migrations phải deterministic.

---

# 54. SAVE ATOMICITY

Save phải an toàn.

Không được:

ghi một phần rồi crash khiến toàn world mất.

Sử dụng:

* transaction;
* temp records;
* versioning;
* checksums/hash nếu phù hợp;
* commit marker.

Nếu save bị gián đoạn:

phải phục hồi phiên bản gần nhất hợp lệ.

---

# 55. SAVE CORRUPTION TESTING

Phải test:

* reload giữa lúc save;
* đóng tab;
* refresh;
* browser crash simulation;
* storage full;
* quota exceeded;
* record malformed;
* schema version old;
* schema version newer;
* missing chunk;
* partially written data.

Game phải phát hiện dữ liệu hỏng thay vì âm thầm sử dụng nó.

---

# 56. BACKUP

Tạo backup save metadata.

Nếu world corruption:

cho phép phục hồi save gần nhất nếu kiến trúc hỗ trợ.

Backup không được gây duplicate world hoặc ghi đè nhầm.

---

# 57. WORLD SEED

Seed phải:

* hiển thị;
* lưu;
* khôi phục;
* dùng được để tái tạo terrain.

Nếu thay đổi generator version, không được giả vờ rằng seed vẫn tạo world y hệt.

Lưu:

generatorVersion.

---

# 58. WORLD GENERATOR VERSIONING

Ví dụ:

generatorVersion = 1

Sau khi thay đổi thuật toán:

generatorVersion = 2.

Old worlds phải tiếp tục hoạt động.

Không regenerate toàn bộ saved chunks chỉ vì game update.

---

# 59. ENTITY PERSISTENCE

Entity quan trọng phải được serialize.

Không được:

* chest mất đồ;
* mob duplication;
* dropped item duplication;
* NPC state mất;
* boss reset ngoài ý muốn.

Dropped items cần lifecycle.

---

# 60. ITEM DROP SYSTEM

Item drop phải có:

* UUID nếu cần;
* itemId;
* quantity;
* position;
* velocity;
* age;
* pickup cooldown.

Không được duplicate khi:

mob death được xử lý hai lần.

---

# 61. CHEST / CONTAINER SYSTEM

Container phải có inventory riêng.

Opening chest:

→ lock/ownership logic nếu cần

→ load inventory

→ show UI.

Closing:

→ flush changes.

Không được mất item nếu tab blur hoặc menu đóng bất ngờ.

---

# 62. NPC / VILLAGE-LIKE SYSTEM

Game có thể có settlement nguyên bản.

NPC có:

* schedule;
* home;
* work;
* dialogue;
* trade;
* daily routine.

Không cần copy NPC của Minecraft.

Hãy tạo hệ thống riêng.

NPC phải tránh:

* đi xuyên block;
* rơi vô hạn;
* stuck forever.

---

# 63. TRADING

Trade UI phải:

* validate input;
* validate output;
* check quantity;
* execute transaction.

Không được exploit bằng:

* double click;
* reopen UI;
* drag race;
* hotbar transfer;
* refresh.

---

# 64. PROGRESSION

Game cần progression.

Ví dụ:

Stage 1:

* basic tools;
* basic blocks;
* surface exploration.

Stage 2:

* metal tools;
* deeper caves.

Stage 3:

* rare resources;
* dangerous zones.

Stage 4:

* advanced crafting.

Stage 5:

* endgame structures.

Không khóa game vào một tuyến duy nhất.

Người chơi phải có tự do.

---

# 65. SURVIVAL SYSTEM

Có thể có:

* health;
* hunger;
* stamina hoặc energy;
* temperature nếu phù hợp;
* status effects.

Nhưng đừng thêm hệ thống chỉ để có thêm thanh UI.

Mỗi survival stat phải đóng góp vào gameplay.

---

# 66. HEALTH

Health phải nhất quán.

Damage sources:

* fall;
* mob;
* environmental;
* fire;
* fluid;
* special.

Không được có double damage do cùng event được dispatch hai lần.

---

# 67. HUNGER

Nếu có hunger:

phải tác động gameplay.

Không để nó chỉ tồn tại cho có.

Nếu player starving:

* hiệu ứng;
* movement;
* health interaction.

Mọi behavior phải được kiểm thử.

---

# 68. STATUS EFFECTS

Có thể:

* poison;
* burning;
* regeneration;
* slow;
* haste-like effect;
* resistance;
* water breathing-like effect.

Mỗi effect:

* duration;
* amplifier;
* source;
* stacking rule;
* expiration.

Không có timer bị leak.

---

# 69. TIME MANAGEMENT

Không dùng setInterval vô trách nhiệm cho mọi thứ.

Game loop là nguồn thời gian chính cho realtime gameplay.

Timer hệ thống cần:

* owner;
* cancellation;
* lifecycle.

Khi entity chết:

các timer liên quan phải được cleanup.

---

# 70. FIXED TIMESTEP

Các hệ thống physics quan trọng có thể dùng fixed timestep.

Render chạy theo frame.

Gameplay simulation không được phụ thuộc hoàn toàn vào FPS.

Nếu máy lag:

game không được tăng tốc bất thường.

---

# 71. PAUSE SYSTEM

Khi pause:

* physics dừng;
* mob AI dừng;
* timers gameplay dừng;
* particles có thể dừng;
* UI vẫn hoạt động.

Không để “pause” chỉ là overlay nhưng thế giới vẫn chạy.

Đối với single-player.

---

# 72. TAB BACKGROUND

Browser tab có thể bị throttling.

Khi:

visibilitychange → hidden

phải xác định behavior.

Không để game:

* teleport player;
* xử lý một deltaTime khổng lồ;
* kill player do lag;
* spawn vô số mobs.

Clamp deltaTime.

---

# 73. DELTA TIME

Không bao giờ tin deltaTime tuyệt đối.

Clamp:

MAX_DELTA.

Ví dụ conceptual:

dt = min(rawDt, MAX_DELTA)

Các hệ thống khác nhau có thể cần fixed timestep.

---

# 74. INPUT PRIORITY

Nếu inventory mở:

movement input không được vô tình thao tác thế giới.

Nếu chat mở:

keyboard không điều khiển player.

Nếu menu mở:

combat không xảy ra.

Input mode phải rõ ràng.

---

# 75. MENU SYSTEM

Có:

* pause;
* inventory;
* crafting;
* settings;
* world menu;
* save/load;
* help;
* controls.

Menu state machine rõ ràng.

Không có:

menu mở chồng vô hạn;

event listener duplicate;

ESC đóng sai cấp.

---

# 76. UI/UX

UI phải hiện đại.

Không chỉ là panel HTML xấu.

Sử dụng:

* hierarchy;
* spacing;
* readable typography;
* animation;
* feedback;
* responsive layout.

Các action quan trọng phải dễ hiểu.

---

# 77. RESPONSIVE

Desktop:

* keyboard + mouse.

Laptop:

* trackpad fallback.

Tablet:

* touch.

Mobile:

* touch controls.

Không được để UI desktop vỡ trên màn hình nhỏ.

---

# 78. TOUCH CONTROL

Touch control phải có:

* movement pad;
* look area;
* jump;
* action;
* hotbar;
* inventory.

Touch event cần xử lý:

touchstart;

touchmove;

touchend;

touchcancel.

Không duplicate pointer + touch events dẫn đến double action.

---

# 79. ACCESSIBILITY

Hỗ trợ:

* configurable sensitivity;
* color considerations;
* text readability;
* scalable UI;
* keyboard navigation cho menu;
* reduced effects;
* reduced motion option.

Không bắt người chơi phải dùng một kiểu input duy nhất.

---

# 80. AUDIO

Audio phải tạo cảm giác thế giới sống.

Có:

* bước chân theo block;
* mining;
* placement;
* inventory;
* crafting;
* combat;
* mob sounds;
* weather;
* caves;
* water;
* ambient;
* UI.

Không được copy soundtrack Minecraft.

Có thể dùng Web Audio để tạo original synthesized effects nếu không có asset.

---

# 81. AUDIO ENGINE

Audio system có:

* master volume;
* music volume;
* effects volume;
* ambient volume;
* mute;
* device resume handling.

Browser autoplay restrictions phải được xử lý.

AudioContext không được crash game nếu chưa user gesture.

---

# 82. SPATIAL AUDIO

Nếu phù hợp:

* distance attenuation;
* stereo panning;
* positional sounds.

Nhưng không tạo quá nhiều AudioNode mỗi frame.

Pool/reuse nếu cần.

---

# 83. MUSIC

Âm nhạc phải nguyên bản.

Hãy tạo ambient themes:

* daytime;
* nighttime;
* cave;
* danger;
* exploration;
* boss;
* special area.

Music transitions mượt.

---

# 84. ERROR HANDLING

Đây là yêu cầu bắt buộc.

Mọi asynchronous operation phải xử lý:

* rejection;
* timeout;
* cancellation;
* malformed result.

Không được lạm dụng:

try { ... } catch {}

Nếu bắt exception:

phải:

* xử lý;
* log hữu ích;
* hoặc chuyển sang fallback.

Không được nuốt lỗi.

---

# 85. CONSOLE KHÔNG PHẢI THƯỚC ĐO

Một game hoàn toàn có thể:

console sạch

nhưng vẫn có:

* item duplication;
* save corruption;
* collision bug;
* memory leak;
* rendering glitch;
* race condition;
* invisible state corruption;
* broken interaction;
* stuck AI;
* deterministic mismatch.

Do đó:

“không có console error”

KHÔNG ĐƯỢC coi là:

“game không có lỗi”.

---

# 86. ERROR OBSERVABILITY

Tạo debug layer có thể bật/tắt.

Có các counters:

* chunks loaded;
* chunks active;
* chunks generated;
* meshes;
* entities;
* particles;
* worker jobs;
* save operations;
* errors;
* warnings;
* frame time.

Debug UI chỉ bật trong development.

Production có thể disable.

---

# 87. ASSERTIONS

Trong development:

assert invariants.

Ví dụ:

inventory count >= 0

entity health >= 0

chunk state valid

block ID valid

NaN không được tồn tại trong position.

Không cho:

NaN;

Infinity;

negative stack;

invalid entity reference.

---

# 88. NaN / INFINITY DEFENSE

Các giá trị:

position.x

position.y

position.z

velocity

rotation

health

damage

time

phải được kiểm tra nếu có nguy cơ.

Nếu NaN xuất hiện:

fail loudly trong dev.

Không tiếp tục lan truyền NaN qua toàn bộ world.

---

# 89. STATE INVARIANTS

Tạo invariant checks cho:

Player

World

Inventory

Chunk

Entity

Save

Crafting

Combat.

Ví dụ:

blockId phải thuộc registry.

Chunk coordinates phải integer.

Inventory slot không có quantity âm.

Entity chết không được target.

Loaded chunk không được có null mesh state ngoài trạng thái hợp lệ.

---

# 90. UNIT TESTS

Viết unit tests cho:

* coordinate math;
* chunk mapping;
* noise;
* deterministic RNG;
* inventory;
* stacking;
* recipes;
* crafting;
* durability;
* damage;
* status effect;
* save serialization;
* migrations;
* item drops;
* spawn validation.

Không test hình thức.

Test edge case.

---

# 91. PROPERTY-BASED TESTING

Nếu có thể, dùng property-based testing.

Ví dụ:

Với mọi số nguyên worldX/worldZ:

chunk mapping roundtrip phải đúng.

Với mọi inventory:

sum quantities không âm.

Với mọi recipe valid:

craft không tạo item từ hư không.

Với mọi serialized object hợp lệ:

deserialize(serialize(x)) ≈ x.

---

# 92. FUZZ TESTING

Fuzz:

* inventory actions;
* block placement;
* chunk coordinates;
* save data;
* recipe input;
* entity spawn;
* player movement;
* UI sequence.

Ví dụ ngẫu nhiên:

open inventory

move item

close

open crafting

craft

move item

refresh

save

reload

Phải không corrupt state.

---

# 93. DETERMINISM TEST

Chạy world generation:

Seed A.

Lần 1 tạo chunks.

Lần 2 tạo cùng chunks nhưng thứ tự khác.

Kết quả phải tương đương.

Nếu khác:

đó là bug.

---

# 94. CHUNK ORDER TEST

Generate:

chunk 0,0

rồi 1,0

rồi 0,1.

Sau đó:

1,0

0,1

0,0.

Terrain phải giống nhau.

Đây là test bắt buộc.

---

# 95. SAVE/LOAD ROUND TRIP TEST

Test:

create world

build structure

break block

craft items

move player

spawn entities

save

reload

compare state.

State sau reload phải tương đương state trước save.

---

# 96. SAVE STRESS

Chạy:

save 100 lần.

Không được:

* duplicate records;
* memory growth vô hạn;
* corruption.

---

# 97. RELOAD STRESS

Test:

load/unload world liên tục.

Đặc biệt:

50+

chu kỳ nếu môi trường test cho phép.

Không có:

* duplicate event handlers;
* duplicate workers;
* memory leak;
* entity duplication.

---

# 98. LONG-RUN TEST

Game không chỉ test 5 phút.

Phải có soak test.

Mô phỏng:

* khám phá;
* mining;
* combat;
* chunk streaming;
* inventory;
* save;
* UI open/close.

Trong thời gian dài.

Theo dõi:

* memory;
* worker count;
* entity count;
* event handlers;
* performance.

---

# 99. MEMORY LEAK TEST

Một pattern quan trọng:

load chunk

→ unload

→ load

→ unload

lặp lại.

Nếu memory cứ tăng bất thường:

điều tra.

---

# 100. EVENT LISTENER LEAK

Các component UI:

mount

→ unmount

→ mount

không được đăng ký event listener lặp.

Có thể dùng:

AbortController

hoặc hệ thống cleanup tập trung.

---

# 101. OBJECT POOL TESTING

Pool phải:

* acquire;
* release;
* reset đầy đủ.

Một object reused không được giữ:

* old position;
* old owner;
* old state;
* old listener;
* old particle data.

---

# 102. ENTITY DESPAWN TEST

Mob chết:

→ removed.

Dropped item hết lifetime:

→ removed.

Chunk unload:

→ entity serialize nếu cần.

Không để references tồn tại.

---

# 103. GARBAGE COLLECTION PRESSURE

Không tạo hàng triệu temporary arrays.

Trong hot loops:

ưu tiên:

* typed arrays;
* reusable buffers;
* preallocated structures.

Không tối ưu mù quáng.

Chỉ tối ưu phần nóng.

---

# 104. MAIN THREAD BUDGET

Mọi frame:

gameplay + render preparation + UI

phải có budget.

Heavy work:

* world generation;
* pathfinding;
* mesh generation;
* save serialization

nên đẩy sang worker khi hợp lý.

---

# 105. WORKER MESSAGE SIZE

Không gửi object khổng lồ qua postMessage nếu có thể tránh.

Ưu tiên:

* ArrayBuffer;
* transferable;
* compact data.

Nhưng không hy sinh tính rõ ràng vô lý.

---

# 106. ASSET LOADING

Asset loader cần:

* cache;
* retry;
* timeout;
* fallback.

Asset load failure không được crash game toàn bộ.

Nếu texture lỗi:

fallback material.

Nếu audio lỗi:

game vẫn chơi được.

---

# 107. OFFLINE

Game có thể hoạt động offline sau lần tải cần thiết.

Nếu PWA phù hợp:

service worker.

Nhưng service worker không được làm build/deploy phức tạp đến mức nguy hiểm.

---

# 108. CACHE VERSIONING

Asset cache cần version.

Khi build mới:

cache bust.

Không để browser sử dụng asset cũ với JS mới.

---

# 109. BROWSER COMPATIBILITY

Test những browser hiện đại chính.

Không phụ thuộc một API experimental mà không fallback nếu không cần.

Kiểm tra:

* WebGL support;
* IndexedDB;
* pointer lock;
* audio;
* workers.

Nếu unsupported:

thông báo rõ ràng.

---

# 110. WEBGL CONTEXT LOSS

Nếu renderer hỗ trợ:

webglcontextlost

và

webglcontextrestored.

Game phải:

* detect;
* pause;
* rebuild resources;
* resume hoặc reload renderer.

Không crash im lặng.

---

# 111. RESIZE

Xử lý:

* browser resize;
* DPR change;
* fullscreen;
* orientation.

Renderer và camera phải đồng bộ.

Không stretch sai aspect ratio.

---

# 112. FULLSCREEN

Fullscreen phải:

* vào;
* thoát;
* update viewport;
* không mất pointer lock;
* không mất input.

---

# 113. POINTER LOCK

Pointer lock denied hoặc lost:

UI phải phản hồi.

Không để mouse look kẹt ở trạng thái giả.

---

# 114. UI EVENT DUPLICATION

Một click không được:

* trigger action hai lần;
* craft hai lần;
* mua hai lần;
* equip hai lần.

Test:

single click;

double click;

rapid click;

pointerdown + click interaction.

---

# 115. ANIMATION

Animation phải:

* smooth;
* time-based;
* pause-aware;
* cancel-aware.

Không dùng animation riêng lẻ không được cleanup.

---

# 116. VISUAL FEEDBACK

Mỗi gameplay action quan trọng phải phản hồi:

* visual;
* audio;
* UI.

Ví dụ:

mining:

progress + sound + particles.

hit:

flash + sound + knockback.

craft:

UI feedback + sound.

---

# 117. DEBUG MODE

Có thể bật:

* hitboxes;
* chunk borders;
* block coordinates;
* FPS;
* entity counts;
* collision;
* AI target;
* path;
* light values.

Debug mode không được phá gameplay.

---

# 118. AUTOMATED E2E

Viết E2E test cho flow:

Launch

→ New World

→ Spawn

→ Move

→ Look

→ Break block

→ Pick item

→ Open inventory

→ Craft

→ Place block

→ Save

→ Reload

→ Verify.

Đây là smoke test bắt buộc.

---

# 119. DEEP E2E

Flow dài hơn:

New World

→ collect resources

→ craft tool

→ explore cave

→ collect rare ore

→ encounter enemy

→ combat

→ place structure

→ save

→ reload

→ continue.

---

# 120. RANDOMIZED E2E

Tạo random action sequences.

Ví dụ:

movement;

jump;

attack;

mine;

place;

inventory;

craft;

save;

reload.

Sau mỗi action:

assert invariants.

Không cần kiểm tra mọi frame bằng snapshot; kiểm tra state correctness.

---

# 121. VISUAL TESTING

Console sạch chưa đủ.

Cần kiểm tra:

* screenshots;
* render output;
* UI states;
* clipping;
* missing textures;
* broken meshes;
* z-fighting;
* black screen;
* pink/magenta material;
* invisible object;
* wrong transparency.

Nếu tooling cho phép:

visual regression tests.

---

# 122. BLACK SCREEN DEFENSE

Game startup phải có watchdog.

Nếu renderer:

* không initialize;
* canvas black;
* asset deadlock;

phải hiện trạng thái rõ ràng.

Không để:

“màn hình đen và không biết tại sao”.

---

# 123. DEADLOCK DEFENSE

Mọi loading process phải có timeout.

Ví dụ:

chunk generation không thể chờ vô hạn.

asset load không thể chờ vô hạn.

save không thể pending vĩnh viễn.

UI loading không thể spinner mãi.

---

# 124. RETRY POLICY

Retry phải giới hạn.

Không:

infinite retry.

Ví dụ:

3 attempts.

Sau đó:

fallback/error.

---

# 125. RESOURCE QUOTA

IndexedDB quota có thể đầy.

Phải xử lý.

Nếu save thất bại:

không được báo “saved successfully”.

Hiện thông báo.

Giữ runtime state an toàn nhất có thể.

---

# 126. STORAGE FAILURE

Nếu IndexedDB unavailable:

game có thể vào fallback mode nếu phù hợp.

Ví dụ:

temporary session-only world.

Nhưng phải cảnh báo người chơi.

Không giả vờ persistent.

---

# 127. SAVE FEEDBACK

UI phải cho thấy:

Saving…

Saved

Save failed

Restoring…

Không spam toast mỗi frame.

---

# 128. WORLD AUTOSAVE

Autosave có interval hợp lý.

Ngoài ra save khi:

* major structure change;
* important progression;
* player quits.

Nhưng không save toàn world mỗi block update theo cách gây lag.

Dirty region/chunk strategy.

---

# 129. DIRTY DATA

Chỉ save thứ đã thay đổi khi có thể.

Ví dụ:

dirtyChunks.

dirtyPlayer.

dirtyEntities.

---

# 130. WORLD DELETION

Xóa world là destructive.

Yêu cầu confirmation.

Không accidental delete.

---

# 131. MULTIPLE WORLDS

Nếu hỗ trợ:

world list.

Mỗi world có:

* id;
* name;
* seed;
* createdAt;
* modifiedAt;
* thumbnail optional;
* version.

Không load nhầm world.

---

# 132. NEW WORLD FLOW

New World UI:

* name;
* seed optional;
* difficulty;
* world size/render settings nếu có;
* generate.

Không được generate world trước rồi mới lưu metadata theo cách race-prone.

---

# 133. DIFFICULTY

Có thể:

Peaceful-like

Normal-like

Hard-like

Custom.

Difficulty ảnh hưởng:

* enemy;
* hunger;
* damage;
* spawn.

Không hardcode hàng chục nơi.

---

# 134. GAME MODES

Có thể thêm:

Survival

Creative-like

Adventure-like

Hardcore-like.

Nhưng mode phải rõ ràng.

Creative-like vẫn phải nhất quán với game.

---

# 135. CREATIVE MODE

Nếu có:

* free flight;
* unlimited blocks;
* instant break;
* inventory access.

Không dùng creative logic để làm hỏng survival world.

---

# 136. ADVENTURE CONTENT

Có thể thêm challenge structures.

Ví dụ:

dungeon;

boss arena;

resource vault;

ancient machine.

Đảm bảo content tăng chiều sâu thay vì chỉ tăng HP.

---

# 137. ENDGAME

Game phải có endgame.

Không để:

có đủ công cụ tốt nhất

→ hết việc.

Endgame có thể:

* rare dimension-like area;
* ancient structures;
* boss;
* advanced crafting;
* automation;
* exploration;
* achievements;
* rare materials.

Tạo mục tiêu dài hạn.

---

# 138. BOSS

Boss cần:

* telegraphed attacks;
* phases;
* arena;
* drops;
* counters;
* audiovisual feedback.

Boss không chỉ là:

HP ×1000.

---

# 139. ENEMY VARIETY

Enemy phải có vai trò.

Ví dụ:

* melee;
* ranged;
* flying;
* tank;
* swarm;
* ambusher;
* caster;
* burrower.

Các enemy cần buộc player dùng chiến thuật khác nhau.

---

# 140. PASSIVE CREATURES

Creature sinh động hơn.

Có:

* idle;
* movement;
* fear;
* interaction;
* drops.

Tránh behavior hoàn toàn tĩnh.

---

# 141. SPAWN MANAGEMENT

Không spawn mob vô hạn.

Có:

* global cap;
* biome cap;
* distance;
* light;
* structure rules;
* density.

Mob gần player phải được ưu tiên phù hợp.

---

# 142. ENTITY LOD / SLEEP

Entity quá xa:

* giảm tick rate;
* sleep;
* unload.

Nhưng persistent entity phải được save.

Không làm world simulation không thể đoán trước.

---

# 143. AI TICK MANAGEMENT

Không chạy toàn bộ AI mỗi frame.

Có thể:

near entities → high frequency

mid distance → lower frequency

far → sleeping.

---

# 144. WORLD LOADING PRIORITY

Ưu tiên:

1. player chunk.
2. immediate neighbors.
3. movement direction.
4. render distance.
5. background.

---

# 145. GENERATION PRIORITY

Nếu player đang chạy nhanh:

prefetch phía trước.

Không generate sau lưng trước phía trước.

---

# 146. SPEED TEST

Player sprint qua world.

Game không được tạo:

chunk loading black wall liên tục.

Có thể có fallback fog/placeholder terrain trong lúc loading nhưng phải visually acceptable.

---

# 147. WORLD BORDERS

Nếu world vô hạn theo lý thuyết:

thực tế phải có giới hạn kỹ thuật an toàn.

Không để tọa độ quá lớn phá physics.

Floating point precision phải được cân nhắc.

Có thể dùng origin rebasing nếu architecture cho phép.

---

# 148. ORIGIN REBASING

Nếu world lớn:

khi player đi rất xa:

rebase scene coordinates.

World coordinates vẫn giữ integer/chunk position.

Render coordinates gần origin.

Nếu triển khai:

phải test thoroughly.

---

# 149. PHYSICS AND WORLD ORIGIN

Không để origin shift làm:

* player teleport;
* entity duplicate;
* camera jump;
* chunk coordinates sai.

---

# 150. BLOCK REGISTRY

Tạo centralized registry.

Block IDs stable.

Không reorder ID tùy tiện nếu save system dựa trên numeric IDs.

Ưu tiên stable string IDs + registry mapping.

---

# 151. ITEM REGISTRY

Tương tự.

Item IDs phải stable.

---

# 152. SAVE COMPATIBILITY

Không bao giờ thay tên ID một cách vô thức.

Nếu rename:

migration.

---

# 153. DATA VALIDATION

Khi load:

validate data.

Không tin dữ liệu save 100%.

Nếu field missing:

default hợp lý.

Nếu type sai:

repair hoặc fail safely.

---

# 154. SECURITY MỨC GAME WEB

Single-player không cần anti-cheat cấp server.

Nhưng save data không được tin tưởng một cách mù quáng.

Nếu có server/multiplayer sau này:

tách authoritative server architecture.

Không thiết kế client-only logic theo cách khóa đường phát triển sau này.

---

# 155. MODULARITY

Hãy để game có thể mở rộng:

thêm block;

thêm item;

thêm recipe;

thêm mob;

thêm biome;

thêm structure;

mà không cần sửa hàng chục hệ thống.

---

# 156. DATA PACK-LIKE DESIGN

Nếu phù hợp:

data nằm trong JSON/TS configuration.

Nhưng tránh runtime fetching quá nhiều.

Build-time bundling là tốt cho static web.

---

# 157. NO PLACEHOLDER LOGIC

Không được dùng:

TODO

// implement later

mock

fake save

fake inventory

fake AI

fake multiplayer

fake physics

trong code production.

Nếu một hệ thống chưa thể hoàn thiện:

hãy giảm scope hợp lý nhưng làm phần đã chọn thật sự hoạt động.

---

# 158. KHÔNG DÙNG “FAKE 3D”

Game phải là 3D voxel thật.

Không dùng:

* ảnh giả làm world;
* video nền;
* trick 2D giả 3D.

---

# 159. KHÔNG DÙNG DOM CHO GAMEPLAY RENDER

World phải render bằng WebGL/WebGPU.

DOM dành cho:

* menus;
* HUD;
* settings;
* accessibility.

---

# 160. UI DOM PERFORMANCE

Không tạo/xóa hàng nghìn DOM node mỗi frame.

HUD update theo state change.

---

# 161. GAME LOOP

Game loop nên có pipeline rõ:

Input

→ Simulation

→ Physics

→ AI

→ World mutations

→ Animation

→ Camera

→ Render preparation

→ Render

→ UI sync.

Không để hệ thống gọi vòng lặp chéo vô hạn.

---

# 162. EVENT BUS

Nếu dùng event bus:

event names typed.

Listeners cleanup.

Không để event bus trở thành “global spaghetti”.

---

# 163. COMMAND SYSTEM

Gameplay mutations quan trọng có thể dùng command layer.

Ví dụ:

BreakBlockCommand

PlaceBlockCommand

CraftCommand

MoveItemCommand

DamageEntityCommand.

Điều này giúp:

* logging;
* replay;
* undo trong dev;
* testing.

---

# 164. REPLAY / DETERMINISTIC DEBUG

Nếu thực tế:

record important actions.

Có thể replay bug.

Ví dụ:

Seed

*

action sequence

*

timestamp/tick

→ tái hiện.

Đây là cách cực kỳ mạnh để tìm lỗi khó.

---

# 165. BUG REPRODUCTION

Khi phát hiện bug:

không chỉ patch symptom.

Phải xác định:

* trigger;
* root cause;
* affected systems;
* regression risk;
* test preventing recurrence.

---

# 166. REGRESSION TEST

Mỗi bug quan trọng sau khi sửa:

thêm test tái hiện bug.

Không được sửa xong rồi để bug quay lại ở bản sau.

---

# 167. ROOT-CAUSE REQUIREMENT

Không chấp nhận fix dạng:

“thêm timeout 1 giây cho đỡ lỗi”

nếu không hiểu tại sao.

Có thể dùng workaround, nhưng phải hiểu root cause.

---

# 168. CODE REVIEW SELF-CHECK

Trước khi xem task hoàn thành:

tự review.

Kiểm tra:

* duplicated logic;
* dead code;
* unhandled promise;
* unsafe null;
* race condition;
* accidental mutation;
* stale refs;
* incorrect cleanup;
* wrong state transition.

---

# 169. TYPE SAFETY

TypeScript strict mode nếu có thể.

Không lạm dụng:

any.

Không dùng:

as any

để né lỗi type mà không có lý do.

Nếu external API không typed:

tạo boundary type guard.

---

# 170. NULLABILITY

Mọi nullable reference phải được xử lý.

Không:

obj!.field

một cách tùy tiện.

---

# 171. ASYNC SAFETY

Async result phải xác nhận rằng context vẫn còn tồn tại.

Ví dụ:

component unmounted

→ fetch/load hoàn thành

→ không được mutate state đã destroy.

---

# 172. ABORT CONTROLLER

Tận dụng AbortController cho:

* asset load;
* async world generation;
* UI actions;
* long operations.

---

# 173. TIMING RACE

Test sequences:

save + unload

craft + close UI

place block + chunk unload

mob death + despawn

load world + settings change.

Không để race condition tạo trạng thái không hợp lệ.

---

# 174. ATOMIC GAMEPLAY ACTION

Các action quan trọng phải có tính atomic ở cấp logic.

Không để nửa action thực hiện rồi fail.

---

# 175. UI STATE CONSISTENCY

UI luôn đọc từ game state chính.

Ví dụ:

inventory count:

không được tự decrement trước rồi chờ backend.

Prefer optimistic UI chỉ khi rollback chắc chắn.

---

# 176. NOTIFICATION SYSTEM

Thông báo không được spam.

Ưu tiên:

* concise;
* contextual;
* severity levels.

Critical errors khác informational.

---

# 177. LOADING STATES

Mỗi async state có:

idle

loading

success

error

cancelled.

Không để UI stuck ở loading.

---

# 178. SETTINGS PERSISTENCE

Settings save riêng.

Không để setting graphics làm hỏng world save.

---

# 179. CONTROL REMAPPING

Nếu hỗ trợ:

player có thể đổi keybind.

Keybind conflicts phải được phát hiện.

Không cho two mandatory actions trùng mà không cảnh báo.

---

# 180. GAMEPAD

Nếu có thời gian:

gamepad support.

Nhưng chỉ triển khai khi làm đúng.

---

# 181. MOBILE PERFORMANCE

Mobile có:

* lower render distance;
* simplified shadows;
* adaptive particles;
* touch UI.

Không mặc định dùng cấu hình desktop trên mobile.

---

# 182. DEVICE QUALITY DETECTION

Có thể ước lượng:

CPU;

GPU;

screen resolution;

memory hint;

mobile/desktop.

Nhưng không được tin 100%.

Cho người dùng override settings.

---

# 183. ADAPTIVE QUALITY

Adaptive quality chỉ can thiệp khi:

frame time thấp hơn/ngưỡng cao hơn trong nhiều frames liên tục.

Không đổi chất lượng theo từng frame.

---

# 184. PERFORMANCE REGRESSION GATE

Mỗi build quan trọng:

benchmark representative scenes.

Theo dõi:

startup;

chunk generation;

mesh generation;

combat;

high mob density;

high particle density.

Nếu regression lớn:

investigate.

---

# 185. STARTUP PERFORMANCE

Initial page:

* minimal JS blocking;
* lazy-load heavy systems khi phù hợp;
* show loading progress;
* no endless blank screen.

---

# 186. FIRST PLAYABLE

Goal:

user từ mở page đến gameplay nhanh nhất có thể trong giới hạn kỹ thuật.

Không preload mọi thứ nếu chưa cần.

---

# 187. SAVE ICON

HUD có icon saving.

Nhưng không gây phiền.

---

# 188. DEATH SYSTEM

Khi player chết:

* rõ nguyên nhân;
* camera feedback;
* death state;
* respawn;
* inventory rule;
* save update.

Không có tình trạng:

player chết nhưng input vẫn điều khiển cơ thể cũ.

---

# 189. RESPAWN

Respawn safe.

Nếu spawn point bị phá:

fallback safe location.

---

# 190. BED / REST / CHECKPOINT-LIKE SYSTEM

Có thể có điểm nghỉ.

Nếu triển khai:

* lưu vị trí;
* danger validation;
* reload persistence.

Không copy nguyên tên/asset Minecraft.

---

# 191. WORLD INTERACTION OBJECTS

Có thể thêm:

* furnace-like workstation;
* storage;
* crafting station;
* portal-like objects;
* machines.

Mỗi object có state.

---

# 192. FURNACE / PROCESSING

Processing system:

input

→ process time

→ output.

Phải pause/resume đúng.

Save progress.

---

# 193. AUTOMATION

Game có thể có automation.

Ví dụ:

* conveyors;
* machines;
* switches;
* power network;
* sensors.

Nhưng hệ thống phải nguyên bản.

Không cần copy Redstone.

---

# 194. SIGNAL SYSTEM

Nếu có:

signal levels;

input;

output;

wiring;

updates.

Chống infinite loops.

Có recursion/update cap.

---

# 195. AUTOMATION LOOP SAFETY

Một hệ thống machine không được gây:

while(true)

hoặc chain reaction vô hạn.

Có tick budget.

---

# 196. BUILDING SYSTEM

Building phải vui.

Có:

* grid;
* preview;
* placement feedback;
* rotation;
* block variants.

Có thể thêm:

copy/paste trong creative mode.

---

# 197. BLUEPRINT

Optional advanced feature:

Blueprint.

Player có thể lưu một cấu trúc rồi tái sử dụng.

Nhưng save data phải được validate.

---

# 198. INTERIOR SYSTEM

Không gian trong nhà phải đẹp.

Lighting.

Shadows.

Block variants.

Furniture nguyên bản.

---

# 199. BLOCK VARIANTS

Đừng chỉ có mỗi block vuông cơ bản.

Có thể có:

* slab-like;
* stair-like;
* pillar;
* wall;
* decorative blocks.

Nếu collision phức tạp:

hãy tạo shape system.

---

# 200. COLLISION SHAPES

Không giả định mọi block full cube.

Có:

FullCube

HalfCube

Slope

Thin

Custom.

Collision system phải deterministic.

---

# 201. RAYCAST SHAPES

Raycast phải phù hợp với collision/visual shape.

Không để player click vào phần invisible của object.

---

# 202. FACE CULLING

Không render mặt block bị che.

Nhưng transparent blocks cần rule riêng.

---

# 203. CHUNK BORDER NEIGHBOR UPDATE

Khi block ở x=chunkWidth-1 thay đổi:

chunk bên cạnh phải biết.

Tương tự:

x=0;

z=0;

z=max.

Đây là bug phổ biến phải test.

---

# 204. CHUNK SEAM TEST

Tạo wall xuyên qua border.

Mine một block ở border.

Kiểm tra visual hai chunk.

Đặt block tại border.

Reload.

Không có seam.

---

# 205. LIGHT BORDER TEST

Light source sát chunk border.

Update.

Unload/reload chunk.

Lighting không được nhảy sai.

---

# 206. ENTITY BORDER TEST

Mob đi qua chunk border.

Không:

duplicate;

disappear;

freeze.

---

# 207. WORLD SAVE BORDER TEST

Structure nằm qua nhiều chunks.

Save.

Reload.

Toàn structure phải nguyên vẹn.

---

# 208. FLOATING BLOCK TEST

Block support removal nếu game có gravity-like blocks.

Nếu block không được phép floating:

update đúng.

---

# 209. FALLING OBJECT SYSTEM

Nếu có physics block:

sand-like;

gravel-like;

hoặc block nguyên bản.

Không cho chain reaction vô hạn.

---

# 210. LIQUID + CHUNK UNLOAD

Nếu fluid đang chảy ở vùng unload:

phải serialize state cần thiết.

Không làm mất fluid hoặc tạo exploit.

---

# 211. FIRE SYSTEM

Nếu có fire:

* spreading limits;
* block immunity;
* duration;
* particles;
* sound.

Không tạo infinite forest fire simulation gây lag.

---

# 212. FARMING

Optional nhưng có giá trị.

Có:

* soil;
* crops;
* growth stages;
* water;
* light;
* harvest.

Growth phải dựa trên world ticks.

Save growth progress.

---

# 213. BREEDING

Optional.

Nếu có creatures:

* compatible pairs;
* cooldown;
* offspring;
* resource cost.

Không spawn vô hạn.

---

# 214. ECONOMY

Nếu có trading/economy:

currency values phải integer-safe.

Không floating precision bug với tiền.

---

# 215. QUEST SYSTEM

Có thể có:

* exploration tasks;
* collection;
* combat;
* construction.

Quest progress lưu.

---

# 216. ACHIEVEMENTS

Optional.

Có thể track:

* first tool;
* first cave;
* first rare ore;
* first boss;
* giant structure.

Không thưởng trùng do duplicate events.

---

# 217. NOTIFICATION EVENTS

Event-based.

Ví dụ:

FIRST_CAVE_ENTERED

RARE_ORE_FOUND

BOSS_DEFEATED.

Event phải idempotent nếu achievement chỉ mở một lần.

---

# 218. INTRODUCTION

New player không được bị ném vào world mà không hiểu gì.

Có onboarding ngắn.

Nhưng không ép tutorial dài.

Player có thể bỏ qua.

---

# 219. DISCOVERY

Thông tin được khám phá qua gameplay:

* recipe;
* world landmarks;
* hints;
* item descriptions.

Không biến game thành danh sách nhiệm vụ bắt buộc.

---

# 220. WORLD ATMOSPHERE

Thế giới phải có sự sống.

Layer:

* sky;
* clouds;
* fog;
* sunlight;
* ambient particles;
* distant terrain;
* sounds;
* wildlife;
* weather.

---

# 221. SKY SYSTEM

Có:

* sun;
* moon-like body;
* stars;
* clouds;
* color gradient.

Không cần giống Minecraft.

Thiết kế bản sắc riêng.

---

# 222. FOG

Fog distance nên tương quan với render distance.

Không fog sát mặt đất một cách khó chịu.

Settings cho phép điều chỉnh.

---

# 223. CLOUDS

Nếu có:

dùng texture/mesh nhẹ.

Không tạo hàng trăm object.

---

# 224. ENVIRONMENTAL AUDIO

Cave:

echo-like ambiance.

Forest:

leaves/wind.

Water:

flow.

Night:

different ambience.

Không copy sound library gốc.

---

# 225. BLOCK SOUND MATERIAL

Block categories:

wood;

stone;

metal;

crystal;

soil;

sand;

glass;

organic.

Mining/placement sound thay đổi theo material.

---

# 226. FOOTSTEP SYSTEM

Footstep dựa trên surface.

Player đi trên:

stone

→ sound A.

grass

→ sound B.

wood

→ sound C.

Nếu block không biết material:

fallback.

---

# 227. CAMERA FEEDBACK

Không lạm dụng shake.

Hit nhẹ.

Explosion có thể shake.

Boss attack mạnh hơn.

Có option disable excessive motion.

---

# 228. PARTICLE QUALITY

Quality setting tác động max particles.

Không chỉ đổi một con số không có hiệu lực.

---

# 229. EFFECT POOLS

Explosion:

pool.

Hit:

pool.

Dust:

pool.

---

# 230. TEXTURE FILTERING

Pixel-like art có thể dùng nearest filtering.

Stylized smooth art có thể dùng linear.

Quyết định nhất quán.

Không random per texture.

---

# 231. COLOR MANAGEMENT

Không để một số texture quá sáng hoặc quá tối ngoài ý muốn.

Test:

daylight;

night;

cave;

fog;

weather.

---

# 232. LIGHT CLAMPING

Không cho lighting values vượt range gây artifacts.

---

# 233. PHYSICS CLAMP

Velocity và movement không được Infinity.

---

# 234. ENTITY HEALTH CLAMP

Health:

max(0, min(maxHealth, value))

theo design.

---

# 235. INVENTORY CLAMP

Quantity:

0 <= quantity <= maxStack.

---

# 236. WORLD COORDINATE SAFETY

Không parse string coordinate không kiểm tra.

Tọa độ phải được validate.

---

# 237. HASH COLLISION / IDS

Nếu dùng generated IDs:

đảm bảo collision unlikely hoặc explicit UUID strategy.

Persistent IDs không nên thay đổi.

---

# 238. SAVE CHECKSUM

Nếu phù hợp, mỗi major save record có integrity metadata.

Nếu checksum mismatch:

mark corrupted.

---

# 239. BACKUP RESTORE TEST

Corrupt một chunk save.

Game phải:

detect.

Không silently accept broken state.

---

# 240. MIGRATION TEST MATRIX

Test:

old version → current.

Missing field.

Extra field.

Renamed field.

Deprecated field.

Invalid enum.

---

# 241. RELEASE MIGRATION

Migration phải chạy một lần.

Không lặp.

Không thay đổi data bất ngờ mỗi load.

---

# 242. BUILD PIPELINE

Production build phải:

* compile;
* typecheck;
* lint nếu dùng;
* test;
* bundle;
* asset validation.

Không deploy nếu build failed.

---

# 243. TYPECHECK GATE

Không coi warning TypeScript là lỗi có thể bỏ qua nếu nó liên quan gameplay correctness.

---

# 244. LINT

Lint phải hỗ trợ phát hiện:

* unreachable;
* unsafe;
* unused;
* suspicious comparisons;
* promises.

---

# 245. TEST GATE

Các test critical phải pass.

Không skip test để pipeline xanh.

Không đổi:

test.skip

chỉ để release.

---

# 246. BROKEN TEST POLICY

Nếu test fail:

điều tra.

Không sửa test để phù hợp với bug.

---

# 247. SNAPSHOT REVIEW

Nếu dùng snapshot:

chỉ cập nhật snapshot khi output thay đổi có chủ đích.

---

# 248. BROWSER E2E

Nếu tooling cho phép:

test Chromium-based browser.

Có thể bổ sung Firefox/WebKit smoke test.

---

# 249. LOW-END TEST

Không chỉ máy mạnh.

Test ở performance profile thấp.

Mục tiêu:

game degrade gracefully.

---

# 250. HIGH-DENSITY TEST

Test:

* nhiều mobs;
* nhiều particles;
* nhiều blocks modified;
* nhiều chunk changes.

Không crash.

---

# 251. RAPID ACTION TEST

Spam:

mine/place/mine/place.

Không duplication.

---

# 252. RAPID MENU TEST

Mở/đóng inventory/settings/crafting liên tục.

Không stuck input.

---

# 253. SAVE WHILE ACTION

Save trong khi:

* mining;
* crafting;
* moving;
* combat.

Không corrupt.

---

# 254. REFRESH TEST

Refresh tại:

* cave;
* water;
* high altitude;
* near structure;
* during combat;
* after placing blocks.

State phải đúng.

---

# 255. CRASH RECOVERY

Nếu tab bị đóng bất ngờ:

autosave strategy phải giảm mất mát.

---

# 256. MULTI-TAB

Nếu multiple tabs mở cùng world:

phải chọn policy.

Không silently cho phép hai tab ghi đè nhau nếu kiến trúc không hỗ trợ.

Tốt nhất phát hiện conflict.

---

# 257. WORLD LOCK

Có thể dùng local lock metadata.

Nếu tab A đang mở world:

tab B cảnh báo.

---

# 258. SAVE RACE

Nếu nhiều save request:

serialize/queue.

Không ghi song song không kiểm soát.

---

# 259. ASSET VALIDATION

Build script phải phát hiện:

* missing asset;
* wrong dimensions;
* unsupported format;
* malformed texture;
* duplicate IDs.

---

# 260. DATA VALIDATION

Validate:

blocks;

items;

recipes;

entities;

biomes;

structures.

Một registry lỗi phải fail build sớm.

---

# 261. CONTENT CONSISTENCY

Mỗi item drop phải tồn tại.

Mỗi recipe ingredient phải tồn tại.

Mỗi texture ID phải tồn tại.

Mỗi mob loot table phải hợp lệ.

Không runtime discover.

---

# 262. DEAD CONTENT DETECTION

Nếu có asset/data không được sử dụng:

có thể cảnh báo.

---

# 263. FEATURE FLAGS

Feature mới có thể được behind flag.

Nhưng không để code dead forever.

---

# 264. DEBUG COMMANDS

Development-only commands:

give item;

teleport;

spawn mob;

time set;

set weather;

regenerate chunk;

inspect block.

Không ship cheat commands vào production nếu không cần.

---

# 265. PROFILING

Có profiler hooks:

* update time;
* physics time;
* AI time;
* mesh time;
* render prep;
* save time.

---

# 266. CHUNK PROFILING

Track:

generation duration;

mesh duration;

memory.

---

# 267. AI PROFILING

Track:

AI ticks;

pathfinding jobs;

average path cost.

---

# 268. SAVE PROFILING

Track:

serialize duration;

write duration;

bytes written.

---

# 269. INPUT PROFILING

Không có input lag do UI/event architecture.

---

# 270. LATENCY OF INTERACTION

Block break/placement phải phản hồi gần như tức thì trong local single-player.

Không đợi save hoàn thành mới show result.

---

# 271. VISUAL PREDICTION

Có thể update visual ngay sau successful gameplay validation.

Save bất đồng bộ sau đó.

---

# 272. FAILURE FEEDBACK

Nếu action thất bại:

giải thích.

Ví dụ:

“Không đủ vật liệu.”

“Không thể đặt block tại vị trí này.”

“Kho lưu trữ đã đầy.”

Không im lặng.

---

# 273. USER FLOW

New user:

Launch

→ main menu

→ new world

→ spawn

→ immediately understand:

move;

look;

break;

place;

inventory.

---

# 274. MAIN MENU

Không cần quá phức tạp.

Nhưng phải đẹp.

Có:

Continue/New World

Settings

Controls

About.

---

# 275. LOADING SCREEN

Loading screen có:

* progress;
* rotating tips;
* world seed optional;
* visual identity.

Không fake progress nếu có thể.

---

# 276. PROGRESS ACCURACY

Nếu progress chỉ ước lượng:

đừng giả 100% rồi đứng đó.

---

# 277. ERROR SCREEN

Critical initialization failure:

hiển thị:

* short message;
* retry;
* diagnostic ID;
* optional details.

---

# 278. NO SILENT FAILURE

Nếu system không thể hoạt động:

phải:

* fallback,
* hoặc cảnh báo.

Không silently disable tính năng quan trọng.

---

# 279. NO FALSE SUCCESS

Đây là nguyên tắc tuyệt đối.

Không viết:

“Save successful”

khi save chưa commit.

Không viết:

“Asset loaded”

khi load failed.

Không viết:

“World generated”

khi còn chunk bắt buộc đang lỗi.

Không nói với người dùng rằng game hoàn thành chỉ vì build pass.

---

# 280. COMPLETION DEFINITION

Một feature chỉ được coi là complete khi:

* implementation tồn tại;
* code compile;
* typecheck pass;
* automated tests pass;
* manual/automated functional test pass;
* edge cases đã kiểm tra;
* cleanup đúng;
* performance hợp lý;
* save/load đúng nếu persistent;
* UI phản ánh đúng state;
* không có known critical defect.

---

# 281. DEFINITION OF DONE CỦA TOÀN GAME

Game chỉ được coi là release candidate khi:

1. Build production thành công.
2. Typecheck sạch.
3. Critical tests pass.
4. E2E smoke pass.
5. Save/load round trip pass.
6. World generation deterministic pass.
7. Chunk border tests pass.
8. Inventory invariants pass.
9. Crafting transaction tests pass.
10. Entity lifecycle tests pass.
11. No known critical gameplay bug.
12. No known save corruption issue.
13. Không có memory leak nghiêm trọng đã biết.
14. Performance đủ ổn định trong target.
15. Game có thể chơi từ đầu đến endgame loop mà không cần developer cheat.
16. UI không có nút chết.
17. Không có asset thiếu bắt buộc.
18. Browser refresh không phá world.
19. Background tab không tạo trạng thái sai.
20. Visual inspection pass.
21. Audio functional pass.
22. Mobile/touch smoke test pass nếu mobile được hỗ trợ.
23. Error recovery đã thử.
24. Regression suite pass.

---

# 282. KHÔNG CHO PHÉP TỰ TUYÊN BỐ “100% BUG-FREE”

Bạn không được sử dụng câu:

“Game 100% không có bug”

nếu chỉ dựa vào:

* console;
* unit tests;
* lint;
* build.

Thay vào đó:

phải báo cáo trung thực:

* tests passed;
* tests failed;
* known limitations;
* unsupported browsers;
* performance constraints;
* remaining risks.

Mục tiêu engineering vẫn là:

**không để lại lỗi đã biết và không bỏ qua các lỗi có thể tái hiện.**

---

# 283. BUG SEVERITY

Phân loại:

P0 — game không khởi động / mất world / corruption.

P1 — gameplay core bị phá.

P2 — major feature sai.

P3 — minor UX issue.

P4 — cosmetic.

Không release với P0/P1.

P2 chỉ chấp nhận khi có lý do rõ ràng và không ảnh hưởng core loop.

---

# 284. CRITICAL BUG EXAMPLES

Các lỗi phải coi là critical:

* player mất inventory;
* save corruption;
* world không load;
* infinite loop;
* browser freeze;
* chunk generation corruption;
* duplicate item exploit nghiêm trọng;
* physics soft-lock;
* game không thể tiếp tục;
* entity duplication phá world state.

---

# 285. SOFT-LOCK DETECTION

Tìm mọi tình huống:

* player kẹt;
* UI kẹt;
* loading kẹt;
* save kẹt;
* quest kẹt;
* interaction kẹt.

Mỗi màn hình/game state cần có exit path hợp lệ.

---

# 286. HARD-LOCK DETECTION

Game không được:

* crash loop;
* load loop;
* save loop;
* infinite loading;
* permanent corrupted state.

---

# 287. RECOVERY DESIGN

Trong những trường hợp bất thường:

* reset transient state;
* reload chunk;
* reopen renderer;
* restore last save;
* retry asset.

Recovery phải có giới hạn để tránh loop vô hạn.

---

# 288. GAMEPLAY BALANCE

Không làm game quá dễ hoặc quá khó.

Tuning dựa trên:

* time-to-first-resource;
* time-to-first-tool;
* time-to-first-danger;
* resource scarcity;
* enemy pressure;
* exploration reward.

Không copy số liệu cụ thể từ Minecraft.

---

# 289. PLAYER MOTIVATION

Game cần tạo lý do để:

* đi xa;
* xuống sâu;
* xây dựng;
* khám phá;
* chế tạo;
* chiến đấu.

Không để mọi thứ chỉ là sandbox trống rỗng.

---

# 290. EXPLORATION REWARDS

Exploration rewards:

* rare resources;
* landmarks;
* recipes;
* cosmetic items;
* lore;
* structures;
* special encounters.

---

# 291. BUILDING REWARD

Cho phép player tự tạo mục tiêu.

Có:

* block variety;
* decorative materials;
* furniture;
* lighting;
* structural shapes.

---

# 292. WORLD SCALE

Thế giới nên tạo cảm giác lớn.

Nhưng đừng tạo procedural infinity chỉ để nói rằng “vô hạn”.

Phải cân bằng:

* world generation;
* save size;
* memory;
* exploration speed.

---

# 293. WORLD DISTANCE

Render distance nên phản ánh:

* hardware;
* selected settings.

---

# 294. FAR TERRAIN

Có thể dùng simplified far representation.

Nhưng tránh:

distant terrain biến dạng mạnh.

---

# 295. TERRAIN CONTINUITY

Không để:

mountain cut;

river dead-end;

floating biome island;

sudden square cliff.

Ngoại lệ có thể có nếu là structure.

---

# 296. SPAWN REGION QUALITY

Spawn region phải có:

* resources;
* shelter potential;
* basic vegetation;
* exploration opportunity;
* not immediate death.

---

# 297. FIRST 10 MINUTES

First 10 minutes phải giúp người chơi:

* hiểu movement;
* hiểu breaking;
* có resource;
* có tool;
* thấy một landmark;
* thấy ít nhất một điểm thú vị.

---

# 298. FIRST HOUR

First hour nên có:

* better gear;
* deeper exploration;
* combat;
* cave;
* rare discovery;
* meaningful construction.

---

# 299. MIDGAME

Midgame có:

* advanced materials;
* stronger enemies;
* special structures;
* improved tools;
* more systems.

---

# 300. LATE GAME

Late game có:

* rare areas;
* bosses;
* advanced automation;
* high-tier construction;
* long-term goals.

---

# 301. ORIGINALITY

Mọi:

* logo;
* game title;
* world lore;
* creature designs;
* UI visuals;
* sounds;
* music;
* texture patterns;
* item names

phải có bản sắc riêng.

Không dùng nội dung Minecraft trực tiếp.

---

# 302. VISUAL IDENTITY

Tạo branding riêng.

Tên tạm có thể do bạn đề xuất trong project.

Không dùng Minecraft trong UI title.

---

# 303. ASSET POLICY

Nếu tự tạo asset:

* original;
* consistent;
* optimized;
* correctly sized;
* compressed;
* loaded efficiently.

Nếu procedural:

visual phải đủ đẹp để không có cảm giác placeholder.

---

# 304. PROCEDURAL MATERIALS

Có thể tạo một phần textures bằng code:

* noise;
* pixel patterns;
* color gradients;
* generated detail.

Nhưng kết quả phải đẹp.

---

# 305. NO EMOJI PLACEHOLDERS

Không dùng emoji như:

🌳

🧱

⚔️

thay cho visual chính của game.

UI icon có thể dùng SVG/canvas asset nguyên bản.

---

# 306. NO PLAIN RECTANGLE WORLD

Voxel có thể vuông về hình học.

Nhưng lighting, material, atmosphere và environmental detail phải tạo chiều sâu.

---

# 307. UI ICONS

Icon cần:

* consistent style;
* clear silhouette;
* readable at small sizes.

---

# 308. FONT

Chọn font web phù hợp license.

Không copy font độc quyền.

Fallback chain chuẩn.

---

# 309. INTERNATIONALIZATION

Nếu có thể:

Vietnamese

English.

Tất cả text gameplay nằm trong localization.

Không hardcode từng câu trong logic.

---

# 310. TEXT EXPANSION

UI phải chịu được text dài hơn.

Không overflow.

---

# 311. SAVE LOCALIZATION

Save phải lưu ID hoặc semantic keys, không lưu text localized như source of truth.

---

# 312. ACCESSIBILITY TEXT

Tooltips có.

Tên block/item rõ.

---

# 313. CONTEXTUAL TOOLTIP

Tooltips không hiện quá lâu hoặc quá nhiều.

---

# 314. ERROR COPY

Thông báo lỗi phải:

* rõ;
* ngắn;
* không đổ lỗi người dùng;
* cho biết hành động cần làm.

---

# 315. PERFORMANCE BUDGETS

Đặt budget thực tế.

Ví dụ conceptual:

startup JS budget;

frame update budget;

mesh generation budget;

save budget.

Nếu vượt:

profile.

---

# 316. PERFORMANCE MODE

Có debug performance overlay.

---

# 317. LOG LEVELS

Development:

debug/info/warn/error.

Production:

giảm log.

Không spam console hàng frame.

---

# 318. LOGGER

Tạo centralized logger.

Có context:

system;

event;

world coordinate;

entity ID.

---

# 319. TELEMETRY

Không cần external telemetry nếu không được yêu cầu.

Nếu có analytics:

privacy-friendly.

Không gửi save/world data nhạy cảm.

---

# 320. PRIVACY

Không thu thập dữ liệu cá nhân không cần thiết.

---

# 321. FILE SIZE

Bundle không nên phình vô kiểm soát.

Dùng code splitting khi hợp lý.

---

# 322. TREE SHAKING

Dependencies phải có lý do.

Không cài 20 library cho tính năng có thể code bằng 50 dòng.

---

# 323. DEPENDENCY AUDIT

Kiểm tra:

unused;

vulnerable;

outdated nếu tooling hỗ trợ.

Nhưng đừng update dependency lớn ngay trước release mà không test.

---

# 324. LOCKFILE

Commit lockfile.

---

# 325. REPRODUCIBLE BUILD

Build nên tái lập ở mức hợp lý.

---

# 326. ENVIRONMENT

Không hardcode local path.

Không phụ thuộc máy developer.

---

# 327. HOSTING

Game phải hoạt động khi deploy trên static hosting nếu kiến trúc là client-only.

Asset paths phải tương đối và đúng base path.

---

# 328. ROUTING

Nếu game là SPA:

refresh route không được 404 khi host hỗ trợ hạn chế.

Nếu cần:

thiết kế route đơn giản.

---

# 329. DEPLOYMENT PATH

Test build trong đúng môi trường production-like.

Không chỉ chạy dev server.

---

# 330. HTTPS

Features như:

* service workers;
* some Web APIs

có thể cần secure context.

Thiết kế hosting phù hợp.

---

# 331. BUILD OUTPUT VALIDATION

Sau build:

kiểm tra asset references.

Không có:

404 asset.

---

# 332. PRODUCTION SMOKE

Mở production URL.

Từ trang trắng:

launch game.

Tạo world.

Play.

Save.

Reload.

---

# 333. CACHE-BUST TEST

Deploy build mới.

Browser hard reload.

Old cache không phá app.

---

# 334. FAILURE INJECTION

Chủ động mô phỏng:

* asset failure;
* storage failure;
* worker failure;
* save failure;
* corrupted data;
* context loss;
* resize;
* tab hidden;
* rapid input.

Game phải degrade gracefully.

---

# 335. CHAOS TESTING

Không phải toàn bộ production.

Development test:

randomly delay:

chunk generation;

asset load;

save;

AI.

Mục tiêu:

phát hiện race condition.

---

# 336. LATENCY INJECTION

Tạo artificial delay 0–1000 ms cho async systems.

Nếu architecture đúng:

game vẫn giữ consistency.

---

# 337. OUT-OF-ORDER RESULTS

Worker result:

job 1

job 2

Nếu job 2 xong trước job 1:

không để job 1 overwrite state mới.

---

# 338. DUPLICATE RESULT

Nếu worker gửi duplicate result:

hệ thống phải idempotent.

---

# 339. CANCELLED RESULT

Result từ cancelled task phải bị bỏ qua.

---

# 340. WORLD EDIT TRANSACTION ID

Có thể dùng revision:

chunkRevision.

Mesh generated for revision 5 không được overwrite revision 6.

---

# 341. MESH VERSIONING

Mỗi chunk có meshVersion.

Render system chỉ accept current version.

---

# 342. ENTITY VERSIONING

Entity async action phải xác nhận entity còn tồn tại/version phù hợp.

---

# 343. UI VERSIONING

Async UI data phải xác nhận screen/context vẫn mở.

---

# 344. SAVE VERSIONING

Async save phải có revision.

Save revision 10 không được overwrite revision 11.

---

# 345. INPUT QUEUE

Nếu cần:

gameplay commands theo queue.

Không giữ input cũ quá lâu.

---

# 346. PHYSICS NUMERICAL STABILITY

Kiểm tra các tình huống:

large velocity;

large dt;

edge collisions;

corner collisions.

---

# 347. COLLISION EPSILON

Dùng epsilon nhất quán.

Không tạo “magic epsilon” khác nhau khắp code.

---

# 348. RAYCAST EPSILON

Block selection phải ổn định trên face boundaries.

---

# 349. BLOCK FACE SELECTION

Crosshair placement phải chính xác.

Không đôi khi chọn block phía sau do floating precision.

---

# 350. INTERACTION RANGE

Range phải được centralize.

Không có:

raycast 5 block;

placement 6 block;

interaction 4 block

một cách vô lý.

---

# 351. CROUCH / SQUEEZE

Nếu có crouch:

player collider đổi đúng.

Không cho player đứng lại trong block.

---

# 352. SWIMMING

Swimming phải có:

buoyancy;

speed modifier;

camera behavior;

oxygen nếu có.

---

# 353. FALL DAMAGE

Falling damage phải dựa trên fall state thật.

Không damage chỉ vì:

teleport;

chunk load;

origin rebasing.

---

# 354. TELEPORT

Teleport system phải:

* validate destination;
* load chunk;
* collision check;
* set velocity;
* camera update.

---

# 355. CHUNK PRELOAD BEFORE TELEPORT

Nếu teleport tới vùng chưa load:

load/preload trước hoặc handle transition.

---

# 356. SPAWN PROTECTION

Nếu game có:

initial period safety.

---

# 357. DAMAGE INVULNERABILITY

Damage immunity frames nếu cần.

Phải reset đúng.

---

# 358. COMBAT COOLDOWNS

Cooldowns phải reset đúng khi:

death;

reload;

weapon switch.

---

# 359. TARGETING

Entity target không được giữ reference dead entity.

---

# 360. DEATH CLEANUP

Death:

* stop AI;
* cancel attacks;
* stop timers;
* drop loot once;
* remove after transition.

---

# 361. BOSS PHASE STATE

Boss phase transitions atomic.

Không trigger phase 2 hai lần.

---

# 362. SCRIPTED EVENTS

Nếu có scripted event:

must be idempotent.

---

# 363. WORLD EVENT SCHEDULER

Nếu có:

storm;

boss;

merchant;

rare event.

Scheduler phải:

* persistent if needed;
* deterministic where needed;
* cancelable.

---

# 364. PLAYER RESTART

Restart world:

dispose all systems.

Không chỉ reset player object.

Phải cleanup:

* chunks;
* workers;
* event listeners;
* audio;
* particles;
* UI;
* timers.

---

# 365. FULL GAME RESET TEST

Create world A.

Play.

Quit.

Create world B.

Play.

Load A.

Play.

Không được world state lẫn nhau.

---

# 366. MEMORY CROSS-WORLD TEST

World A unload hoàn toàn.

World B load.

Không giữ references A ngoài cache chủ định.

---

# 367. CACHE INVALIDATION

Cache phải có key gồm:

worldId;

version;

coordinate.

Không lấy mesh world A cho world B.

---

# 368. WORLD ISOLATION

Hai world có cùng seed nhưng ID khác:

save data không được trộn.

---

# 369. INVENTORY ISOLATION

Player A/B hoặc world A/B không share inventory accidentally.

---

# 370. SETTINGS ISOLATION

Global settings có thể shared.

World settings phải tách nếu thiết kế cần.

---

# 371. DATA CLONING

Không mutate template data.

Ví dụ:

BLOCK_TEMPLATE

không được dùng trực tiếp làm mutable runtime object cho mọi block.

---

# 372. IMMUTABILITY BOUNDARIES

Static registries immutable.

Runtime state mutable.

---

# 373. SERIALIZATION

Không serialize class instance bằng cách mù quáng.

Serialize plain data.

---

# 374. DESERIALIZATION

Construct runtime object từ validated plain data.

---

# 375. SCHEMA VALIDATOR

Nếu dùng validator:

mọi external/save data đi qua validation.

---

# 376. BACKWARD COMPATIBILITY

Không phá world cũ vì refactor nội bộ.

---

# 377. VERSIONED FORMAT

Version rõ ràng.

---

# 378. MIGRATION ROLLBACK

Nếu migration fail:

giữ original backup.

Không overwrite dữ liệu duy nhất.

---

# 379. CRASH-RESISTANT SAVE

Nguyên tắc:

Never destroy last known good save before new save commit.

---

# 380. UX SAVE SAFETY

Khi đang save quan trọng:

UI phản ánh.

---

# 381. WORLD EXIT

Khi quit:

flush critical data.

Nhưng không block vô thời hạn.

---

# 382. PAGE UNLOAD

Dùng appropriate browser lifecycle APIs, nhưng không phụ thuộc hoàn toàn vào unload event.

Autosave strategy phải chịu trách nhiệm chính.

---

# 383. BEFOREUNLOAD

Không lạm dụng.

Chỉ cảnh báo khi thực sự nguy cơ mất dữ liệu.

---

# 384. NETWORK-LESS GAMEPLAY

Core gameplay không phụ thuộc mạng nếu đây là single-player.

---

# 385. FUTURE MULTIPLAYER

Thiết kế boundary để sau này có thể:

* authoritative world;
* player state;
* server commands.

Nhưng không cần fake multiplayer.

---

# 386. NO FAKE MULTIPLAYER

Không tạo UI “Multiplayer” chỉ để trông hoàn chỉnh nếu backend chưa tồn tại.

---

# 387. FEATURE HONESTY

Chỉ hiển thị feature đã hoạt động.

---

# 388. CONTENT DENSITY

Game phải có đủ content để world không cảm giác procedural empty.

---

# 389. LANDMARK SYSTEM

Tạo landmark silhouette dễ nhận biết.

---

# 390. DISCOVERY MAP

Optional.

Nếu có:

player-created map hoặc simple compass.

Không cần clone map UI của Minecraft.

---

# 391. COMPASS

Nếu có:

point north;

spawn;

landmark.

---

# 392. MINIMAP

Optional.

Nếu có:

không render toàn world bằng DOM.

---

# 393. MAP PERFORMANCE

Map update incremental.

---

# 394. INVENTORY UX

Drag/drop responsive.

Touch drag support.

Keyboard shortcuts.

---

# 395. ITEM DESCRIPTION

Tooltip:

name;

type;

stats;

use.

---

# 396. STACK SPLITTING

Half stack.

Single item.

Bulk move.

Không duplication.

---

# 397. DRAG CANCEL

Nếu drag ra ngoài:

item trở về slot source hoặc valid fallback.

Không drop item vào void.

---

# 398. EQUIPMENT

Nếu có armor:

slots;

stats;

durability;

visual optional.

---

# 399. EQUIPMENT TRANSACTION

Equip/unequip atomic.

---

# 400. ITEM USE

Food/potion/item use có cooldown.

Không consume hai lần do rapid clicks.

---

# 401. HOTKEYS

Action mapping centralized.

---

# 402. MOBILE ACTION BUTTONS

Không tạo touch UI che màn hình quá mức.

---

# 403. CROSSHAIR

Crosshair rõ ràng.

Hit state có feedback.

---

# 404. BLOCK HIGHLIGHT

Block targeted có outline/subtle highlight.

Không gây z-fighting.

---

# 405. PLACEMENT PREVIEW

Ghost block translucent.

Không ảnh hưởng collision.

---

# 406. FIRST-PERSON BODY

Optional hand/tool representation.

Nếu làm:

không clipping nghiêm trọng.

---

# 407. VIEWMODEL

Nếu có:

tách khỏi world renderer.

---

# 408. ANIMATION BLENDING

Movement animations blend.

Không snap giữa states.

---

# 409. CREATURE ANIMATION

Simple but readable.

---

# 410. ENTITY LOD VISUALS

Far entities simplified.

---

# 411. AI VISIBILITY

Mobs không cần perceive player qua toàn bộ world.

Raycast/visibility checks.

---

# 412. LIGHT-BASED SPAWN

Nếu sử dụng light:

tính light query hiệu quả.

---

# 413. NAVIGATION REGION

Không pathfind qua:

void;

solid wall;

lava nếu mob không immune;

deep water nếu không aquatic.

---

# 414. MOB PERSONALITY

Có thể thêm:

aggressive;

timid;

territorial;

nocturnal.

Tăng chiều sâu.

---

# 415. ENVIRONMENTAL HAZARDS

Có thể:

spores;

toxic cave;

heat zone;

cold zone.

Nhưng mỗi hazard phải có counterplay.

---

# 416. BOSS REWARD

Boss reward không được phá economy.

---

# 417. ECONOMY TUNING

Theo dõi:

resource inflow;

resource outflow.

Không để resource vô hạn do farm exploit.

---

# 418. DUPLICATION EXPLOITS

Test:

inventory + chest;

craft + inventory;

death drop + reload;

save + duplicate;

rapid interaction.

---

# 419. ITEM DUPLICATION FUZZ

Randomized operations trong inventory/container phải giữ tổng item invariant nếu không có intentional creation event.

---

# 420. RESOURCE CONSERVATION

Trong giao dịch bình thường:

total input + intentional outputs

phải cân bằng.

---

# 421. CURRENCY CONSERVATION

Same.

---

# 422. XP / PROGRESSION

Nếu có XP:

không tăng double do event duplicate.

---

# 423. QUEST PROGRESS

Event idempotent.

---

# 424. ACHIEVEMENT PROGRESS

Không reset sau reload.

---

# 425. WORLD FLAGS

World-wide events có state rõ ràng.

---

# 426. DEBUG SAVE

Development build có thể export save metadata để inspect.

---

# 427. SAVE EXPORT

Optional manual backup:

download world data.

Không export secrets.

---

# 428. SAVE IMPORT

Nếu hỗ trợ:

validate thoroughly.

---

# 429. INVALID IMPORT

Không overwrite current world trước khi validate.

---

# 430. LARGE SAVE IMPORT

Không block UI toàn bộ nếu file lớn.

---

# 431. PROGRESSIVE LOAD

Load essential player data trước.

Chunk data streaming sau.

---

# 432. LOADING PRIORITY

Player spawn region first.

---

# 433. FIRST FRAME

Canvas phải xuất hiện nhanh.

---

# 434. FRAME CONSISTENCY

Không update UI từng pixel mỗi frame nếu không cần.

---

# 435. REACTIVE STATE

Dùng reactive patterns có kiểm soát.

Không over-render.

---

# 436. DOM MEASUREMENT

Tránh forced synchronous layout trong game loop.

---

# 437. CSS

CSS không được gây layout thrashing.

---

# 438. CANVAS

Renderer canvas responsive.

Input coordinate conversion chính xác sau resize/DPR.

---

# 439. POINTER COORDINATES

Mouse raycast phải dựa trên current canvas bounds.

Không hardcode window center.

---

# 440. FULLSCREEN POINTER

Test resolution changes.

---

# 441. TOUCH COORDINATES

DPR independent.

---

# 442. GAMEPAD DEADZONE

Nếu hỗ trợ:

deadzone.

---

# 443. INPUT REPEAT

Đảm bảo key repeat không craft 30 lần khi người chơi giữ phím ngoài ý muốn.

---

# 444. ACTION BUFFER

Nếu cần:

jump buffer.

Nhưng có giới hạn.

---

# 445. COYOTE TIME

Optional movement quality.

---

# 446. MOVEMENT FEEL

Player movement nên:

responsive;

predictable;

not slippery unless intended.

---

# 447. CAMERA SENSITIVITY

Linear/quadratic mapping phải test.

---

# 448. FOV

FOV slider clamped safe range.

---

# 449. SCREEN SHAKE

Configurable.

---

# 450. COLOR BLINDNESS

Không dùng màu duy nhất để truyền thông tin quan trọng.

---

# 451. AUDIO CUES

Quan trọng có audio + visual.

---

# 452. TUTORIAL

Context hints.

Không spam.

---

# 453. HELP MENU

Có controls.

---

# 454. KEYBOARD NAVIGATION

Menu buttons accessible.

---

# 455. FOCUS MANAGEMENT

Khi mở modal:

focus vào modal.

Khi đóng:

focus trở lại trigger.

---

# 456. ARIA

Các UI control cần semantic labels nếu DOM-based.

---

# 457. LOCAL STORAGE

Chỉ dùng cho:

settings;

small metadata.

Không lưu world lớn bằng localStorage.

---

# 458. INDEXEDDB

World data.

---

# 459. IDB TRANSACTION

Batch writes hợp lý.

---

# 460. IDB ERROR

Onerror handling.

---

# 461. IDB VERSION CHANGE

Blocked event phải được xử lý.

---

# 462. MULTI-TAB IDB

Thông báo conflict nếu upgrade blocked.

---

# 463. SAVE QUEUE

Có một save coordinator trung tâm.

---

# 464. SAVE BACKPRESSURE

Nếu người chơi thay đổi quá nhanh:

coalesce saves.

Không queue hàng nghìn.

---

# 465. WORLD MUTATION QUEUE

Có thể batch nearby edits.

---

# 466. RENDER INVALIDATION

Chỉ rebuild mesh khi chunk dirty.

---

# 467. LIGHT INVALIDATION

Chỉ update light affected region.

---

# 468. COLLISION INVALIDATION

Chỉ recompute affected chunk/region.

---

# 469. AI INVALIDATION

Terrain change có thể invalidate path.

---

# 470. PATH CACHING

Cache path nếu phù hợp.

Không dùng cache sau world mutation lớn nếu stale.

---

# 471. STALE CACHE

Mọi cache phải có invalidation rule.

Không được cache “vĩnh viễn” mà không biết khi nào cần refresh.

---

# 472. BLOCK DATA CACHE

Immutable registry.

---

# 473. TEXTURE CACHE

Single source.

---

# 474. AUDIO CACHE

Reuse buffers.

---

# 475. MODEL CACHE

Reuse geometry/material.

---

# 476. MEMORY BUDGET

Đặt giới hạn cache.

LRU nếu cần.

---

# 477. CHUNK CACHE

Không giữ quá nhiều chunk ngoài active radius trừ khi cần.

---

# 478. PRELOAD

Preload chỉ trong reasonable radius.

---

# 479. USER CONFIGURATION

Render distance user configurable.

Không ép một giá trị duy nhất.

---

# 480. DEFAULT CONFIGURATION

Chọn conservative defaults để game ổn định trên nhiều máy.

---

# 481. QUALITY AUTO

Cho user switch manual.

---

# 482. ERROR REPORTING

Development report:

system;

error;

stack;

state;

seed;

chunk coordinates.

---

# 483. BUG SNAPSHOT

Khi assertion fail:

capture useful diagnostics.

---

# 484. DETERMINISTIC RNG

Mỗi subsystem có RNG stream nếu cần.

Ví dụ:

world;

loot;

mob;

weather.

Không share một RNG global theo cách làm thay đổi kết quả chỉ vì load order.

---

# 485. RNG TEST

same seed + same inputs → same outputs.

---

# 486. LOOT TABLE

Data-driven.

Drops có:

chance;

quantity;

conditions.

---

# 487. LOOT DUPLICATION

Death event idempotent.

---

# 488. CHEST LOOT

Generated once.

Chest loot seed/state saved.

Không reroll mỗi load.

---

# 489. STRUCTURE LOOT

Same principle.

---

# 490. CHEST OPENING

Open state optional.

Nếu chest can be opened infinitely:

loot must not regenerate accidentally.

---

# 491. WORLD EVENT RANDOMNESS

Persistent random events phải save seed/state cần thiết.

---

# 492. WEATHER RANDOMNESS

Không để reload thay đổi weather theo cách exploitable nếu không chủ đích.

---

# 493. DAY/NIGHT RANDOMNESS

Không reset.

---

# 494. MOB SPAWN RNG

Không phụ thuộc chunk load order theo cách phá determinism nếu determinism là requirement.

---

# 495. CONTENT PIPELINE

Tạo tools/scripts để validate data.

---

# 496. ASSET PIPELINE

Texture atlas generation tool nếu hữu ích.

---

# 497. ICON PIPELINE

Generate icon set consistent.

---

# 498. SOUND PIPELINE

Central manifest.

---

# 499. BUILD VALIDATION

Fail fast.

---

# 500. TEST MATRIX

Tạo matrix:

Feature × Browser × Device × State.

Không cần exhaustive mọi combination nhưng critical paths phải phủ.

---

# 501. EDGE CASE MATRIX

Player:

* at spawn;
* at world border;
* under terrain;
* inside cave;
* in water;
* falling;
* dead;
* inventory open;
* menu open;
* tab hidden.

Test interactions.

---

# 502. INPUT EDGE MATRIX

* click during loading;
* key press before world ready;
* mouse move during menu;
* ESC multiple times;
* double click;
* rapid press/release.

---

# 503. WORLD EDGE MATRIX

* chunk negative coordinates;
* chunk positive;
* border;
* max loaded;
* unloaded region;
* regenerated region.

---

# 504. SAVE EDGE MATRIX

* empty world;
* huge world;
* many dirty chunks;
* active entities;
* mid-combat;
* low storage;
* interrupted save.

---

# 505. INVENTORY EDGE MATRIX

* empty;
* full;
* stack max;
* stack split;
* invalid item;
* drag outside;
* simultaneous actions.

---

# 506. CRAFTING EDGE MATRIX

* missing ingredient;
* exact ingredient;
* extra ingredient;
* output full;
* output partial;
* locked recipe;
* rapid click.

---

# 507. COMBAT EDGE MATRIX

* target dies same frame;
* multiple attackers;
* block between;
* death during attack;
* reload during combat.

---

# 508. AI EDGE MATRIX

* target despawns;
* path blocked;
* destination unloaded;
* path too long;
* no route.

---

# 509. RENDER EDGE MATRIX

* context lost;
* resize;
* DPR change;
* texture missing;
* many chunks;
* many transparent objects.

---

# 510. AUDIO EDGE MATRIX

* autoplay blocked;
* context suspended;
* missing sound;
* rapid sound event;
* too many simultaneous sounds.

---

# 511. RECOVERY MATRIX

For each system:

failure;

detection;

fallback;

recovery;

user notification.

---

# 512. TEST AUTOMATION

Automate as many regression tests as reasonable.

Không chỉ manual testing.

---

# 513. MANUAL QA

Cuối cùng vẫn phải có manual play session.

Chơi như người dùng.

Không dùng dev shortcuts.

---

# 514. BLIND PLAYTEST

Trong một vòng test:

tắt debug tools.

Chơi chỉ bằng public UI.

Phát hiện UX issues.

---

# 515. STRESS PLAYTEST

Trong vòng khác:

* sprint continuously;
* mine;
* combat;
* build;
* travel.

Theo dõi performance.

---

# 516. CHAOTIC PLAYTEST

Cố tình làm những điều người dùng nghịch:

* spam;
* open/close;
* place/remove;
* jump everywhere;
* cross chunk borders;
* save repeatedly.

---

# 517. EXPLORATION PLAYTEST

Đi thật xa khỏi spawn.

Mục tiêu:

phát hiện streaming issues.

---

# 518. DEEP UNDERGROUND PLAYTEST

Xuống vùng rất sâu.

Test:

* lighting;
* caves;
* ores;
* navigation;
* performance.

---

# 519. HIGH ALTITUDE PLAYTEST

Test:

sky;

fog;

falling;

terrain.

---

# 520. WATER PLAYTEST

Test:

swim;

enter;

exit;

fluid updates;

audio.

---

# 521. NIGHT PLAYTEST

Test:

mob spawn;

lighting;

audio;

weather.

---

# 522. STORAGE FULL PLAYTEST

Mock quota failure.

Game phải không mất toàn bộ save.

---

# 523. WORKER FAILURE PLAYTEST

Terminate worker.

Game phải fallback/recover.

---

# 524. RENDERER FAILURE PLAYTEST

Simulate context loss nếu tooling cho phép.

---

# 525. NETWORK FAILURE

Nếu static client-only game:

core không phụ thuộc network.

Asset load failure phải có fallback.

---

# 526. NO EXTERNAL AI DEPENDENCY

Game không được phụ thuộc live AI service để gameplay cơ bản hoạt động.

---

# 527. NO REMOTE CODE EXECUTION

Không tải JavaScript executable arbitrary từ third-party.

---

# 528. SUPPLY CHAIN SAFETY

Dependencies tối thiểu.

---

# 529. BUILD SIZE

Không nhồi dependency không cần.

---

# 530. DOCUMENTATION

Tạo README rõ ràng:

* setup;
* dev;
* build;
* test;
* architecture;
* save format;
* known limitations.

---

# 531. ARCHITECTURE DOCUMENT

Có sơ đồ conceptual:

Input

→ Game State

→ World

→ Physics/AI

→ Rendering

→ UI

→ Save.

---

# 532. DEBUG DOCUMENTATION

Giải thích cách bật:

* debug;
* profiling;
* test world;
* deterministic seed.

---

# 533. TEST DOCUMENTATION

Các command:

npm run test

npm run e2e

npm run build

npm run typecheck

hoặc tương đương.

---

# 534. DEVELOPMENT COMMANDS

Đừng yêu cầu người dùng chạy 20 command khó hiểu.

Tạo scripts rõ.

---

# 535. ONE-COMMAND START

Có thể:

npm install

npm run dev.

Production:

npm run build.

---

# 536. ONE-COMMAND QA

Tạo:

npm run verify

để chạy:

typecheck

lint

unit tests

build

và test cần thiết.

---

# 537. ZERO KNOWN FAILURE POLICY

Nếu npm run verify fail:

không tuyên bố done.

---

# 538. TEST REPORT

Sau mỗi major milestone:

ghi:

PASS/FAIL.

---

# 539. FAILURE LOG

Không chỉ nói:

“có lỗi”.

Ghi:

* what;
* why;
* fix;
* test.

---

# 540. FINAL QA REPORT

Trước khi hoàn tất:

xuất report gồm:

Build

Typecheck

Unit Tests

Integration Tests

E2E

Save/Load

Determinism

Performance

Visual

Audio

Browser

Recovery

Known Issues.

---

# 541. ZERO KNOWN CRITICAL BUGS

Mục tiêu release:

0 known P0.

0 known P1.

P2 chỉ khi thực sự cần và phải được ghi rõ.

---

# 542. FEATURE COMPLETENESS

Mỗi core feature phải được đánh dấu:

Implemented

Tested

Integrated

Persisted if necessary

Reviewed.

---

# 543. NO HALF-INTEGRATED FEATURE

Không được có:

button có nhưng system không có;

system có nhưng UI không có;

data có nhưng render không có.

---

# 544. NO UNUSED FEATURE BUTTONS

Nếu feature chưa tồn tại:

không hiển thị button production.

---

# 545. UI COPY CONSISTENCY

Naming consistent.

Không:

“Start World”

ở màn này và

“Create Game”

ở màn khác nếu cùng một action.

---

# 546. GAME FEEL

Ngoài correctness, hãy tinh chỉnh:

* movement responsiveness;
* block break feedback;
* pickup attraction;
* camera response;
* sound layering;
* particle timing;
* UI animation.

---

# 547. JUICE

Thêm polish nơi hữu ích:

* small hit particles;
* screen feedback;
* smooth transitions;
* subtle sounds;
* environmental animation.

Không spam effects.

---

# 548. INTERACTION FEEDBACK DELAY

Input-to-feedback nên rất nhanh.

---

# 549. VISUAL HIERARCHY

World:

foreground;

midground;

background.

---

# 550. READABILITY

Player luôn dễ thấy.

Hostile mob không bị background hòa vào.

Important resources có silhouette/visual cues.

---

# 551. COLOR LANGUAGE

Dùng màu có hệ thống.

Không random.

---

# 552. BIOME PALETTE

Mỗi biome có identity riêng nhưng không phá cohesion.

---

# 553. WEATHER VISIBILITY

Mưa/tuyết không che kín game.

---

# 554. CAVE VISIBILITY

Darkness tạo atmosphere nhưng không biến game thành màn hình đen không thể chơi.

---

# 555. LIGHT SOURCES

Có một số light sources đẹp.

---

# 556. REFLECTIONS

Optional.

Chỉ dùng nếu performance cho phép.

---

# 557. POST PROCESSING

Bloom/contrast/vignette optional.

Không lạm dụng.

---

# 558. GPU FALLBACK

Nếu effect unsupported:

disable effect, giữ gameplay.

---

# 559. LOW END FALLBACK

Tắt:

* shadows;
* bloom;
* particles;

nếu cần.

Gameplay vẫn đúng.

---

# 560. HIGH END ENHANCEMENT

High-end có:

* better shadows;
* more particles;
* greater draw distance;
* enhanced atmosphere.

---

# 561. QUALITY PRESETS TEST

Mỗi preset phải:

* apply;
* persist;
* take effect;
* not crash.

---

# 562. SETTINGS HOT APPLY

Các setting không cần restart phải áp dụng ngay.

Các setting cần reload phải nói rõ.

---

# 563. WORLD SETTINGS

World-specific settings không phá save.

---

# 564. DEFAULT SAFE SETTINGS

Nếu setting corrupt:

fallback default.

---

# 565. CONFIG VALIDATION

Validate numeric values.

No NaN.

---

# 566. LOCALIZATION VALIDATION

Không được thiếu translation key trong production.

Fallback English/Vietnamese nếu thiếu.

---

# 567. LONG TEXT TEST

Text dài phải không phá UI.

---

# 568. FONT LOADING FAILURE

Fallback font.

---

# 569. ACCESSIBILITY CONTRAST

Critical text readable.

---

# 570. MOTION REDUCTION

Reduced motion option.

---

# 571. AUDIO AUTOPLAY

Start music only after legal browser user gesture.

---

# 572. AUDIO CONTEXT SUSPENSION

Resume on first interaction.

---

# 573. AUDIO CLEANUP

World restart không tạo nhiều AudioContext.

---

# 574. MUSIC TRANSITIONS

Crossfade controlled.

Không stack track vô hạn.

---

# 575. SOUND VOICE LIMIT

Có max simultaneous sounds per category.

---

# 576. PRIORITY AUDIO

Important sounds ưu tiên.

---

# 577. UI AUDIO

Không sound mọi hover nếu spam.

---

# 578. SAVE SOUND

Subtle.

---

# 579. ERROR AUDIO

Chỉ khi phù hợp.

---

# 580. GAME OVER AUDIO

Distinct.

---

# 581. CONTENT GENERATION

Có thể tạo nhiều content procedural.

Nhưng phải có validation.

---

# 582. PROCEDURAL STRUCTURE VALIDATOR

Check:

structure inside allowed world;

not floating unless intentional;

not blocking spawn;

loot references valid.

---

# 583. BIOME VALIDATOR

No invalid biome IDs.

---

# 584. SPAWN TABLE VALIDATOR

All mobs valid.

---

# 585. LOOT TABLE VALIDATOR

All items valid.

---

# 586. RECIPE VALIDATOR

All ingredients/items valid.

---

# 587. BLOCK DROP VALIDATOR

Every block drop item exists.

---

# 588. SOUND MATERIAL VALIDATOR

Every material category maps to valid audio.

---

# 589. TEXTURE VALIDATOR

Every texture reference exists.

---

# 590. RENDER MATERIAL VALIDATOR

Every material loaded.

---

# 591. MISSING RESOURCE FALLBACK

Fallback ID must always exist.

---

# 592. GAME START SAFETY

If some optional content fails:

game still starts.

If critical content fails:

fail visibly with diagnostic.

---

# 593. ERROR BOUNDARIES

Subsystem failure should not cascade unnecessarily.

---

# 594. DECOUPLING

Audio failure should not kill world simulation.

UI bug should not corrupt save.

Particle bug should not break physics.

---

# 595. SAVE INDEPENDENCE

Rendering problems must not alter saved state.

---

# 596. RENDER STATE EPHEMERAL

Do not serialize:

mesh;

GPU resources;

renderer objects.

Serialize semantic state only.

---

# 597. PHYSICS STATE

Serialize only necessary persistent state.

Do not serialize transient contact manifolds.

---

# 598. PARTICLE STATE

Usually ephemeral.

---

# 599. AUDIO STATE

Usually ephemeral except music settings.

---

# 600. FINAL ARCHITECTURE PRINCIPLE

Build the game so that:

GAME STATE

is authoritative.

RENDERING

visualizes state.

UI

controls state.

AUDIO

reacts to state.

SAVE

persists state.

WORKERS

compute data safely.

TESTS

protect invariants.

DEBUG TOOLS

expose hidden failures.

---

# 601. PROJECT IMPLEMENTATION ORDER

Bạn phải tự quản lý thứ tự triển khai.

Nhưng một thứ tự hợp lý:

Foundation

→ Renderer

→ Block registry

→ Chunk

→ World generation

→ Player

→ Collision

→ Interaction

→ Inventory

→ Crafting

→ Items

→ Entities

→ AI

→ Save

→ Lighting

→ Audio

→ UI

→ Content

→ Polish

→ QA.

Không tích hợp mọi thứ cùng lúc.

---

# 602. DO NOT BUILD EVERYTHING BLINDLY

Sau mỗi major system:

test.

Không chờ đến cuối rồi mới debug.

---

# 603. MILESTONE GATES

Mỗi milestone phải pass gate.

Milestone 1:

renderer.

Milestone 2:

world.

Milestone 3:

player.

Milestone 4:

interaction.

Milestone 5:

inventory/crafting.

Milestone 6:

entities/combat.

Milestone 7:

save.

Milestone 8:

content/polish.

Milestone 9:

release QA.

---

# 604. FOUNDATION GATE

Không tiếp tục nếu renderer/core unstable.

---

# 605. WORLD GATE

Không tiếp tục nếu chunk/terrain nondeterministic hoặc corruption.

---

# 606. PLAYER GATE

Không tiếp tục nếu collision không đáng tin.

---

# 607. INVENTORY GATE

Không tiếp tục nếu duplication/loss bugs.

---

# 608. SAVE GATE

Không release nếu roundtrip không pass.

---

# 609. PERFORMANCE GATE

Không release nếu ordinary hardware có severe freeze trong core gameplay.

---

# 610. VISUAL GATE

Không release với:

missing textures;

black world;

broken UI;

severe z-fighting.

---

# 611. AUDIO GATE

Không release với:

audio initialization crash;

infinite sound spam.

---

# 612. FINAL PLAYABLE

Cuối dự án phải có:

một world có thể chơi từ đầu;

khám phá;

mine;

craft;

build;

fight;

survive;

save;

reload;

tiến triển;

endgame objective.

---

# 613. FINAL QUALITY BAR

Đừng hỏi:

“Code có chạy không?”

Hãy hỏi:

“Người chơi có thể chơi lâu mà không nhận ra hệ thống bị giả, bị vỡ hoặc không nhất quán không?”

---

# 614. PLAYER PERSPECTIVE

Bạn phải thử chơi như một người không biết code.

Không nhìn vào implementation.

Chỉ nhìn:

* cảm giác;
* phản hồi;
* UI;
* stability;
* fun.

---

# 615. DEVELOPER PERSPECTIVE

Sau đó trở lại vai trò engineer:

* inspect logs;
* inspect memory;
* inspect state;
* inspect timings;
* inspect save.

---

# 616. QA PERSPECTIVE

Cuối cùng cố tình phá game.

Cố:

* spam;
* chạy xa;
* reload;
* resize;
* chuyển tab;
* thay setting;
* destroy/replace;
* craft liên tục;
* combat.

Mục tiêu là tìm bug trước người chơi.

---

# 617. “KHÔNG CÓ LỖI TRÊN CONSOLE” KHÔNG BAO GIỜ ĐƯỢC DÙNG LÀ FINAL PROOF

Lặp lại nguyên tắc:

console sạch chỉ chứng minh một phần rất nhỏ.

---

# 618. HIDDEN BUG CATEGORIES

Phải kiểm tra cả:

1. State bugs.
2. Logic bugs.
3. Numerical bugs.
4. Timing bugs.
5. Async bugs.
6. Concurrency bugs.
7. Memory bugs.
8. Rendering bugs.
9. Input bugs.
10. Save bugs.
11. Migration bugs.
12. Performance bugs.
13. UX bugs.
14. Content reference bugs.
15. Browser lifecycle bugs.
16. Resource exhaustion.
17. Recovery bugs.
18. Determinism bugs.
19. Exploit/duplication bugs.
20. Cross-system integration bugs.

---

# 619. BUG HUNTING MINDSET

Không chỉ hỏi:

“Có error không?”

Hãy hỏi:

“Điều gì sẽ xảy ra nếu thứ tự xảy ra khác đi?”

Ví dụ:

save bắt đầu

→ chunk unload

→ player quit

→ worker result về

→ browser tab hidden.

Tất cả đều phải an toàn.

---

# 620. ORDER-OF-OPERATIONS TESTING

Cùng một hành động được thực hiện theo nhiều thứ tự.

Nếu state kết quả khác nhau ngoài phạm vi design:

có khả năng race condition.

---

# 621. EVENT DUPLICATION

Cùng event dispatch hai lần phải:

* idempotent nếu appropriate;
* hoặc bị chặn.

---

# 622. EVENT LOSS

Nếu event critical bị mất:

state phải vẫn nhất quán bằng cách khác.

---

# 623. EVENT ORDER

Nếu thứ tự event quan trọng:

explicit queue.

Không phụ thuộc incidental JavaScript timing.

---

# 624. ASYNC ORDER

Không assume Promise resolves theo thứ tự tạo.

---

# 625. CANCELLATION

Cancelled task không được mutate state.

---

# 626. RETRY IDEMPOTENCY

Retry action không được duplicate side effect.

---

# 627. TRANSACTION IDEMPOTENCY

Same transaction ID không execute hai lần nếu duplicate request.

---

# 628. DEBUGGING “HEISENBUG”

Thêm logging không được làm thay đổi behavior một cách đáng kể.

---

# 629. TIMING-SENSITIVE BUGS

Có test với artificial delay.

---

# 630. FRAME-RATE VARIANCE

Test game simulation với:

30 FPS;

60 FPS;

120 FPS;

variable FPS.

Gameplay result phải hợp lý.

---

# 631. DELTA-TIME ROBUSTNESS

Không để movement speed khác nhau rõ rệt theo FPS.

---

# 632. PHYSICS CONSISTENCY

Falling và collision phải tương đối ổn định giữa FPS.

---

# 633. AI CONSISTENCY

Mob behavior không được phụ thuộc quá mạnh vào render FPS.

---

# 634. WORLD GENERATION CONSISTENCY

Không phụ thuộc frame timing.

---

# 635. SAVE CONSISTENCY

Không phụ thuộc frame timing.

---

# 636. TAB THROTTLING

Test:

hidden 30 sec;

return.

Không:

teleport;

death by enormous dt;

explosion of timers.

---

# 637. WINDOW FOCUS

Focus loss.

Return.

Input reset.

---

# 638. WINDOW RESIZE STRESS

Resize liên tục trong game.

Không crash.

---

# 639. DEVICE ORIENTATION

Portrait ↔ landscape.

Nếu mobile.

---

# 640. INPUT DEVICE SWITCHING

Mouse → touch/pointer.

Không duplicate input.

---

# 641. ACCESSIBILITY MODE

Reduced motion.

Low effects.

High contrast if implemented.

---

# 642. SAVE FORMAT DOCUMENTATION

Document fields and rationale.

---

# 643. MIGRATION COVERAGE

Mỗi schema version migration có test.

---

# 644. BUILD ARTIFACT

Production output phải có đầy đủ:

HTML

JS

CSS

assets.

---

# 645. STATIC HOSTING

Paths phải hoạt động ở subpath.

Ví dụ:

/game/

không chỉ root.

---

# 646. BASE URL

Không hardcode “/”.

---

# 647. ASSET PATH

Central asset resolver.

---

# 648. CACHE BUSTING

Hashed assets hoặc equivalent.

---

# 649. SOURCE MAPS

Development source maps.

Production policy rõ.

---

# 650. SECURITY HEADERS

Nếu hosting hỗ trợ:

CSP phù hợp.

---

# 651. XSS DEFENSE

User-generated world/name/text:

sanitize/escape.

Không inject raw HTML.

---

# 652. SAVE IMPORT SAFETY

Never eval save data.

Không executable deserialization.

---

# 653. DATA FILE SAFETY

Không execute dynamic code từ JSON.

---

# 654. RANDOM USER CONTENT

Nếu có custom names:

escape UI.

---

# 655. WORLD NAME

Không dùng trực tiếp làm filename path nếu không sanitizing.

---

# 656. EXPORT FILE NAME

Sanitize.

---

# 657. DOWNLOAD HANDLING

Nếu export save:

safe.

---

# 658. NO REMOTE SCRIPT INJECTION

Không tải remote code runtime trừ dependency được kiểm soát.

---

# 659. DEPENDENCY LOCK

Lock versions.

---

# 660. FINAL QA LOOP

Loop:

BUILD

→ TEST

→ RUN

→ BREAK

→ FIX

→ TEST

→ PROFILE

→ RECHECK

→ BUILD

→ FINAL SMOKE.

Không:

BUILD

→ “looks good”

→ done.

---

# 661. FINAL INTERNAL AUDIT

Trước khi hoàn thành hãy tự hỏi:

Nếu tôi là người chơi, điều gì khiến tôi quit?

Nếu tôi là hacker/exploiter, tôi duplicate item bằng cách nào?

Nếu tôi là browser throttling, tôi có phá game không?

Nếu IndexedDB fail thì sao?

Nếu worker trả kết quả cũ thì sao?

Nếu player đi tới chunk âm thì sao?

Nếu renderer mất context thì sao?

Nếu AI target chết thì sao?

Nếu user double-click thì sao?

Nếu save xảy ra giữa transaction thì sao?

Nếu page refresh đúng thời điểm xấu nhất thì sao?

Nếu player chơi 3 giờ thì sao?

Nếu player chạy hàng nghìn blocks thì sao?

Nếu hàng trăm entities tồn tại thì sao?

Nếu memory tăng dần thì sao?

Không được bỏ qua các câu hỏi này.

---

# 662. “3 GIỜ CHƠI” TEST

Giả lập hoặc manual play dài.

Mục tiêu:

* no degradation;
* no leak;
* no state corruption;
* no duplicate;
* no infinite queues.

---

# 663. “1000 CHUNK” CLASS TEST

Trong development/performance environment:

generate/load/unload rất nhiều chunk.

Mục tiêu:

* stable memory;
* bounded workers;
* no mesh leak.

---

# 664. “1000 ACTIONS” TEST

Random player actions.

Sau mỗi 100 actions:

check invariants.

---

# 665. “1000 SAVE” TEST

Nếu tooling phù hợp:

save repeated.

Không corruption.

---

# 666. “10000 BLOCK EDITS” TEST

Mining/placing random.

Check:

* chunk integrity;
* save;
* mesh.

---

# 667. “MASS ENTITY” TEST

Spawn many test entities.

Game degrade gracefully.

No hard crash.

---

# 668. “MASS PARTICLE” TEST

Particle cap works.

---

# 669. “MASS SOUND” TEST

Audio cap works.

---

# 670. “MASS UI OPEN/CLOSE” TEST

No event leak.

---

# 671. “WORLD RESTART” TEST

Repeat.

---

# 672. “BROWSER REFRESH” TEST

At dangerous times.

---

# 673. “BROWSER BACK/FORWARD” TEST

Nếu SPA route có liên quan.

---

# 674. “MULTI-TAB” TEST

Conflict policy.

---

# 675. “STORAGE FULL” TEST

No silent data loss.

---

# 676. “ASSET MISSING” TEST

Fallback.

---

# 677. “WORKER CRASH” TEST

Fallback.

---

# 678. “CONTEXT LOSS” TEST

Recovery.

---

# 679. “LOW FPS” TEST

Gameplay remains stable.

---

# 680. “HIGH FPS” TEST

Gameplay remains stable.

---

# 681. “LARGE DT” TEST

No teleport/explosion.

---

# 682. “NEGATIVE COORDINATE” TEST

All world systems.

---

# 683. “CHUNK BORDER” TEST

All relevant systems.

---

# 684. “SAVE MIGRATION” TEST

Old world.

---

# 685. “CORRUPTED SAVE” TEST

Detect.

---

# 686. “PARTIAL SAVE” TEST

Recover.

---

# 687. “DUPLICATION” TEST

Inventory.

Container.

Crafting.

Drops.

---

# 688. “ITEM LOSS” TEST

Every inventory mutation.

---

# 689. “STATE DRIFT” TEST

Render vs gameplay state.

UI vs gameplay state.

Save vs gameplay state.

---

# 690. “INVISIBLE ERROR” TEST

Errors that don't throw:

* stale state;
* wrong boolean;
* missing update;
* event not delivered;
* wrong cache;
* wrong coordinate;
* wrong reference.

Testing must compare outcomes, not exceptions.

---

# 691. ORACLE-BASED TESTING

Where possible:

expected invariant.

Ví dụ:

break block:

before count + drop = after inventory/world.

---

# 692. DIFFERENTIAL TESTING

Có thể chạy alternative/simple reference implementation cho utilities.

Ví dụ coordinate mapping.

---

# 693. GOLDEN TESTS

Seed + coordinates → known terrain fingerprints.

Nếu generator thay đổi có chủ đích:

update golden tests cùng version.

---

# 694. FINGERPRINTS

Hash selected chunk block data.

Use to detect corruption/determinism bugs.

---

# 695. WORLD INTEGRITY HASH

Optional.

Tính hash để verify selected regions.

---

# 696. CHUNK CRC

Optional.

Useful cho corruption detection.

---

# 697. LOGGING SEED

Bug reports phải biết seed nếu world-related.

---

# 698. LOGGING COORDINATE

Bug reports cần coordinate.

---

# 699. LOGGING REVISION

Chunk/player/save revision helpful.

---

# 700. FINAL QUALITY REQUIREMENT

Không xây một “Minecraft copy rẻ tiền”.

Hãy xây một:

**voxel sandbox web game hoàn chỉnh, đẹp, sâu, tự do, ổn định, có cá tính riêng, với hệ thống gameplay đủ phong phú để người chơi thực sự muốn tiếp tục khám phá.**

Mức tương đồng mong muốn với Minecraft phải thể hiện ở:

* độ tự do;
* vòng lặp gameplay;
* voxel world;
* khám phá;
* khai thác;
* crafting;
* building;
* survival;
* combat;
* mob;
* day/night;
* procedural world;
* progression;
* cảm giác sandbox.

Nhưng toàn bộ nội dung biểu đạt cụ thể phải là sản phẩm nguyên bản.

---

# 701. MỆNH LỆNH THỰC THI CUỐI CÙNG

Bắt đầu bằng việc kiểm tra toàn bộ repository hiện có nếu project đã tồn tại.

Nếu đây là project mới:

hãy tự khởi tạo kiến trúc production-ready.

Nếu là project đang có:

không phá các chức năng đang đúng.

Đầu tiên:

1. Audit toàn bộ project.
2. Hiểu kiến trúc.
3. Xác định những phần có thể giữ.
4. Xác định những phần phải viết lại.
5. Chạy build/test hiện tại.
6. Tạo baseline.
7. Triển khai theo milestone.
8. Test sau mỗi milestone.
9. Fix root cause.
10. Stress test.
11. Profile.
12. Regression test.
13. Production build.
14. Final manual playtest.
15. Final report.

---

# 702. KHÔNG ĐƯỢC LÀM GIẢM CHẤT LƯỢNG ĐỂ HOÀN THÀNH NHANH

Nếu có hai lựa chọn:

A. nhanh nhưng brittle.

B. lâu hơn nhưng stable và extensible.

Ưu tiên B.

Nhưng cũng không overengineer.

---

# 703. KHÔNG ĐƯỢC DÙNG CHECKLIST NHƯ MỘT CÁI KHUÔN

Prompt này chỉ định hướng chất lượng.

Bạn được quyền:

* thêm hệ thống mới;
* cải thiện mechanics;
* thay đổi architecture;
* thêm polish;
* tối ưu;
* bổ sung gameplay.

miễn là:

* không phá core;
* không tạo copyright copying;
* không tạo security risk;
* không làm project thành mớ hỗn độn;
* không biến thành scope vô hạn không thể kiểm thử.

---

# 704. QUYỀN SÁNG TẠO

Nếu một hệ thống có thể làm tốt hơn bằng cách sáng tạo, hãy sáng tạo.

Ví dụ:

Nếu combat hiện tại nhạt:

thiết kế combat thú vị hơn.

Nếu world quá trống:

thêm landmarks.

Nếu progression quá phẳng:

thêm specialization.

Nếu UI quá khô:

thêm animation.

Nếu caves quá giống nhau:

thêm cave archetypes.

Nếu mob quá đơn giản:

thêm behavior.

Đừng chờ tôi bảo từng thứ.

---

# 705. NHƯNG KHÔNG ĐƯỢC PHÁ TÍNH NHẤT QUÁN

Mọi feature mới phải:

* dùng architecture hiện tại;
* có state rõ;
* có save behavior;
* có tests;
* có cleanup;
* có error handling.

---

# 706. NEW FEATURE GATE

Feature mới chỉ thêm nếu:

benefit > complexity risk.

---

# 707. NO FEATURE BLOAT

Không thêm:

100 hệ thống vô nghĩa.

Một feature có chiều sâu tốt hơn 20 feature nông.

---

# 708. PLAYER EXPERIENCE TEST

Mỗi feature phải trả lời:

“Tại sao người chơi quan tâm?”

Nếu câu trả lời không rõ:

đơn giản hóa hoặc bỏ.

---

# 709. WORLD COHESION

Tất cả content phải có cùng artistic direction.

---

# 710. SYSTEM COHESION

Các hệ thống phải tương tác tự nhiên.

Ví dụ:

weather → crops;

light → mob;

terrain → exploration;

ore → crafting;

crafting → progression;

progression → deeper world.

---

# 711. EMERGENT GAMEPLAY

Tạo hệ thống kết hợp để người chơi tự tạo câu chuyện.

Đây là một trong những mục tiêu quan trọng nhất.

---

# 712. PLAYER FREEDOM

Người chơi không nên bị buộc phải chơi đúng một tuyến.

---

# 713. BUILDING AS CORE

Xây dựng phải là một mục tiêu thật sự, không chỉ phụ.

---

# 714. EXPLORATION AS CORE

Thế giới phải có lý do để đi xa.

---

# 715. SURVIVAL AS CORE

Nếu game có survival:

survival phải tạo decision-making.

---

# 716. CRAFTING AS CORE

Crafting phải hỗ trợ progression.

---

# 717. COMBAT AS CORE

Combat cần đủ chiều sâu để không chỉ spam attack.

---

# 718. RESOURCE LOOP

Resources:

common;

uncommon;

rare;

very rare.

Scarcity có lý do.

---

# 719. RISK VS REWARD

Vùng nguy hiểm nên có phần thưởng tương ứng.

---

# 720. DISCOVERY MOMENTS

Game nên tạo các moment:

“Ồ, cái này là gì?”

“Có gì dưới này?”

“Đây là một structure!”

“Cuối cùng mình tìm thấy tài nguyên hiếm!”

---

# 721. SURPRISE

Procedural world không được hoàn toàn predictable.

---

# 722. CONTROLLED RANDOMNESS

Randomness nên có structure.

---

# 723. NO REPETITION FATIGUE

Biomes/structures/mobs phải đủ variation.

---

# 724. WORLD STORYTELLING

Không cần narrative tuyến tính.

Có thể kể chuyện bằng:

* structures;
* environment;
* item descriptions;
* landmarks.

---

# 725. VISUAL STORYTELLING

Một ruined tower phải tự kể được một phần câu chuyện bằng hình ảnh.

---

# 726. SOUND STORYTELLING

Âm thanh cave/weather có thể báo hiệu môi trường.

---

# 727. ENEMY TELEGRAPHING

Người chơi phải hiểu danger.

---

# 728. FAIRNESS

Không death bởi:

bug;

invisible hit;

unreadable mechanic.

---

# 729. PLAYER TRUST

Save system phải đáng tin.

Controls phải phản hồi.

Game không được “lừa” người chơi bằng state sai.

---

# 730. FINAL PLAYER TEST

Đóng tất cả debug.

Khởi động game như user thật.

Không đọc source.

Chỉ chơi.

Sau đó ghi lại:

* friction;
* confusion;
* bugs;
* performance;
* visual issues;
* audio issues.

---

# 731. FINAL ENGINEERING TEST

Bật debug.

Run:

* stress;
* memory;
* deterministic;
* save;
* recovery;
* fuzz.

---

# 732. FINAL RELEASE GATE

Chỉ báo:

“READY”

khi toàn bộ release gate pass.

Nếu chưa:

tiếp tục sửa.

---

# 733. NẾU GẶP LỖI TRONG QUÁ TRÌNH PHÁT TRIỂN

Không giấu lỗi.

Không bỏ qua.

Không viết workaround mù.

Không đánh dấu complete.

Thực hiện:

REPRODUCE

→ ISOLATE

→ ROOT CAUSE

→ FIX

→ TEST

→ REGRESSION

→ VERIFY.

---

# 734. NẾU KHÔNG THỂ TÁI HIỆN

Hãy:

* tăng diagnostics;
* record state;
* record seed;
* record action sequence;
* inject delays;
* repeat under stress.

Không tự kết luận “không sao”.

---

# 735. NẾU TEST PASS NHƯNG GAME VẪN SAI

Tin behavior thực tế.

Test phải được cải tiến.

Đừng sửa game chỉ để chiều test sai.

---

# 736. NẾU PERFORMANCE XẤU

Đầu tiên profile.

Không tối ưu mù.

Xác định bottleneck:

CPU;

GPU;

memory;

I/O;

DOM;

workers.

Sau đó sửa đúng chỗ.

---

# 737. NẾU VISUAL XẤU

Không chỉ tăng post-processing.

Kiểm tra:

* lighting;
* palette;
* materials;
* scale;
* silhouette;
* fog;
* geometry density;
* environment composition.

---

# 738. NẾU GAME NHẠT

Không chỉ thêm 50 item.

Xem:

* progression;
* risk;
* reward;
* exploration;
* emergent systems;
* pacing.

---

# 739. NẾU GAME QUÁ PHỨC TẠP

Giảm complexity không cần thiết.

Core phải dễ hiểu.

---

# 740. NẾU CODE QUÁ PHỨC TẠP

Refactor.

---

# 741. NẾU CODE QUÁ ĐƠN GIẢN ĐẾN MỨC BRITTLE

Thiết kế abstraction cần thiết.

---

# 742. FINAL ARCHITECTURAL HEALTH

Kiểm tra:

coupling;

cohesion;

dependency direction;

testability;

maintainability.

---

# 743. DEPENDENCY DIRECTION

Core không nên phụ thuộc UI.

World không nên phụ thuộc DOM.

Physics không nên phụ thuộc React/UI framework nếu không cần.

---

# 744. RENDERING BOUNDARY

Gameplay state không phụ thuộc GPU objects.

---

# 745. SAVE BOUNDARY

Save layer không phụ thuộc renderer.

---

# 746. AUDIO BOUNDARY

Audio không được là prerequisite cho gameplay.

---

# 747. UI BOUNDARY

UI không phải source of truth.

---

# 748. WORLD BOUNDARY

World simulation độc lập với render distance ở mức logic.

---

# 749. RENDER DISTANCE ≠ SIMULATION RULE

Không để mob tồn tại hay không chỉ vì camera visibility trừ khi design có chủ đích.

---

# 750. SIMULATION DISTANCE

Có thể thấp hơn render distance nhưng policy phải rõ.

---

# 751. ENTITY PERSISTENCE DISTANCE

Persistent entity không bị delete chỉ vì camera đi xa.

---

# 752. DESPAWN POLICY

Có rule rõ:

distance;

population;

persistence.

---

# 753. MOB AI FAIRNESS

AI không teleport xuyên map.

---

# 754. PLAYER VISIBILITY

Player không bị target xuyên tường nếu design không cho phép.

---

# 755. LINE OF SIGHT

Raycast.

---

# 756. PROJECTILE

Nếu có projectile:

* velocity;
* collision;
* lifetime;
* hit;
* despawn.

No infinite projectile.

---

# 757. EXPLOSIONS

Explosion có radius.

Không recursion vô hạn.

Block destruction bounded.

---

# 758. EXPLOSION SAVE

Exploded area dirty chunks.

---

# 759. AREA EFFECTS

Toxic/fire/etc. phải bounded.

---

# 760. TIMER GROUPS

Timers theo owner.

Owner destroyed:

cleanup.

---

# 761. AUDIO OWNER

Sounds associated with destroyed entity phải được stop/fade nếu cần.

---

# 762. PARTICLE OWNER

Particles có thể detach hoặc cleanup.

---

# 763. UI MODAL OWNER

Close screen:

destroy owned listeners.

---

# 764. WORKER OWNER

World destroyed:

terminate/cancel owned jobs.

---

# 765. WORLD MANAGER DISPOSE

Một API:

disposeWorld()

phải cleanup toàn bộ resource của world.

---

# 766. ENGINE DISPOSE

Restart game:

disposeEngine().

---

# 767. TEST DISPOSAL

Test create/destroy loop.

---

# 768. “GHOST RESOURCE” DETECTION

Sau dispose:

workers;

timers;

listeners;

audio contexts;

webgl resources

không được tiếp tục hoạt động ngoài policy.

---

# 769. BROWSER DEVTOOLS TEST

Kiểm tra:

Memory;

Performance;

Application/IndexedDB;

Network;

Console;

Rendering.

Nhưng đừng chỉ dựa vào console.

---

# 770. NETWORK PANEL

Static game không được request loop bất thường.

---

# 771. FAILED RESOURCE REQUESTS

No broken mandatory assets.

---

# 772. INDEXEDDB INSPECTION

Save records phải hợp lý.

---

# 773. MEMORY HEAP SNAPSHOT

Compare after repeated:

load/unload/restart.

---

# 774. PERFORMANCE RECORDING

Capture:

normal;

combat;

chunk streaming;

high density.

---

# 775. FPS FLOOR

Theo dõi minimum/1% low.

---

# 776. FRAME TIME SPIKES

Find spikes.

---

# 777. LONG TASKS

Minimize blocking main-thread long tasks.

---

# 778. JS BUNDLE

Large bundle parse cost phải hợp lý.

---

# 779. LAZY LOAD

Heavy optional modules load when needed.

---

# 780. WORLD GENERATION WORKER

Nếu worker generation:

transfer data efficiently.

---

# 781. MESH WORKER

Có thể tách.

---

# 782. PATHFINDING WORKER

Optional.

---

# 783. SAVE WORKER

Optional nếu serialization nặng.

---

# 784. WORKER ARCHITECTURE

Không tạo một worker cho mỗi chunk.

Pool workers.

---

# 785. WORKER POOL SIZE

Bounded theo hardware.

---

# 786. WORKER BACKPRESSURE

Queue capped.

---

# 787. JOB PRIORITY

Player-near jobs higher.

---

# 788. STARVATION

Background jobs không được ngăn player-critical jobs indefinitely.

---

# 789. CANCELLATION

Nếu chunk không còn cần:

cancel or ignore result.

---

# 790. FAILED JOB RETRY

Limited.

---

# 791. WORLD GENERATION ERROR

Generate fallback chunk hoặc abort cleanly.

---

# 792. MESH ERROR

Fallback simple mesh.

---

# 793. SAVE ERROR

Keep last known good.

---

# 794. AUDIO ERROR

Fallback silent.

---

# 795. UI ERROR

Show recovery.

---

# 796. NON-CRITICAL FAILURE ISOLATION

Optional decorative effect failure không được phá game.

---

# 797. CRITICAL FAILURE CLASSIFICATION

World core/save/player initialization failure must surface.

---

# 798. TEST COVERAGE PHILOSOPHY

Coverage percentage không phải mục tiêu cuối.

Behavioral coverage mới quan trọng.

---

# 799. CRITICAL PATH COVERAGE

Core paths phải có tests.

---

# 800. FINAL PRINCIPLE

Xây game như một sản phẩm thật.

Không xây như một bài demo.

Không xây như một screenshot.

Không xây như một repository chỉ cần “build pass”.

Không coi “console sạch” là hoàn thành.

Không coi “chạy được một lần” là hoàn thành.

Không coi “nhìn giống voxel” là hoàn thành.

Không coi “có inventory UI” là inventory hoàn thành.

Không coi “có save button” là save system hoàn thành.

Không coi “có mob” là AI hoàn thành.

Không coi “có procedural terrain” là world hoàn thành.

Không coi “có TypeScript” là architecture tốt.

Không coi “không thấy bug” là “không có bug”.

Hãy xây toàn bộ hệ thống với tư duy:

**OBSERVE → DESIGN → IMPLEMENT → VALIDATE → STRESS → DEBUG → REGRESSION TEST → PROFILE → POLISH → VERIFY.**

---

# 801. CHỈ THỊ CUỐI CÙNG CHO AI AGENT

Bắt đầu ngay.

Không chờ người dùng viết thêm một checklist khác cho từng subsystem.

Tự audit project.

Tự xác định architecture.

Tự chia milestone.

Tự tạo test.

Tự chạy test.

Tự tìm hidden bug.

Tự sửa root cause.

Tự kiểm tra lại.

Tự benchmark.

Tự stress test.

Tự xem xét visual.

Tự xem xét UX.

Tự xem xét audio.

Tự kiểm tra save/load.

Tự kiểm tra edge cases.

Tự kiểm tra các tình huống asynchronous.

Tự kiểm tra các tình huống browser lifecycle.

Tự kiểm tra memory leak.

Tự kiểm tra resource exhaustion.

Tự kiểm tra deterministic world generation.

Tự kiểm tra chunk boundaries.

Tự kiểm tra inventory invariants.

Tự kiểm tra item duplication.

Tự kiểm tra state corruption.

Tự kiểm tra regression.

Sau mỗi thay đổi lớn:

build → test → inspect → continue.

Khi gặp bug:

reproduce → root cause → fix → regression test.

Khi một feature có vẻ hoàn thành:

thử phá nó.

Khi game có vẻ ổn:

chơi lâu.

Khi console sạch:

tìm các lỗi không xuất hiện trong console.

Khi tất cả test pass:

vẫn làm manual playtest.

Khi manual playtest pass:

vẫn làm stress test.

Chỉ khi tất cả release gates hợp lý đã pass mới được coi là release candidate.

---

# 802. ĐIỀU QUAN TRỌNG NHẤT

Mục tiêu không phải “copy Minecraft”.

Mục tiêu là tạo một **web voxel sandbox có chất lượng đủ cao để người chơi lập tức nhận ra triết lý gameplay quen thuộc của dòng Minecraft-style, nhưng vẫn cảm thấy đây là một trò chơi riêng, có thế giới riêng, hệ thống riêng và bản sắc riêng.**

Hãy hướng tới mức tương đồng rất cao ở trải nghiệm:

* tự do;
* khám phá;
* voxel;
* crafting;
* mining;
* building;
* survival;
* combat;
* procedural world;
* day/night;
* creatures;
* progression;
* emergent gameplay.

Nhưng tuyệt đối không phụ thuộc vào việc sao chép trực tiếp asset hay nội dung biểu đạt của Minecraft.

---

# 803. TIÊU CHUẨN CHẤT LƯỢNG CUỐI

Khi tôi mở game, tôi phải có cảm giác:

“Đây là một game sandbox voxel thật sự.”

Không phải:

“Đây là prototype.”

Không phải:

“Đây là terrain demo.”

Không phải:

“Đây là một trang web giả lập voxel.”

Không phải:

“Đây là một UI mockup.”

Mà là:

**một game hoàn chỉnh có thể khám phá, xây dựng, chiến đấu, chế tạo, sinh tồn, lưu lại và tiếp tục chơi.**

---

# 804. MỤC TIÊU RELEASE

Release Candidate chỉ được tạo khi:

* core gameplay hoạt động;
* world generation ổn định;
* chunk streaming ổn định;
* player physics ổn định;
* inventory ổn định;
* crafting ổn định;
* combat ổn định;
* AI ổn định;
* save/load ổn định;
* graphics ổn định;
* audio ổn định;
* UI ổn định;
* performance hợp lý;
* regression test pass;
* no known critical issues;
* manual playtest pass;
* stress testing pass;
* production build pass.

---

# 805. KHÔNG ĐƯỢC BỎ CUỘC Ở LỖI PHỨC TẠP

Nếu bug khó:

chia nhỏ.

Nếu architecture cũ tệ:

refactor.

Nếu một subsystem không thể cứu:

replace có kiểm soát.

Nếu một optimization gây bug:

rollback optimization và tìm cách khác.

Nếu một feature quá tham vọng:

đơn giản hóa implementation, nhưng vẫn giữ chất lượng.

Không được giảm tiêu chuẩn chỉ để “hoàn thành nhanh”.

---

# 806. FINAL COMMAND

**XÂY GAME.**

**KIỂM TRA GAME.**

**CỐ TÌNH PHÁ GAME.**

**TÌM LỖI.**

**SỬA GỐC RỄ.**

**VIẾT REGRESSION TEST.**

**CHẠY LẠI TOÀN BỘ SUITE.**

**PROFILE PERFORMANCE.**

**KIỂM TRA MEMORY.**

**KIỂM TRA SAVE.**

**KIỂM TRA CHUNK.**

**KIỂM TRA PHYSICS.**

**KIỂM TRA AI.**

**KIỂM TRA UI.**

**KIỂM TRA AUDIO.**

**KIỂM TRA VISUAL.**

**KIỂM TRA BROWSER LIFECYCLE.**

**KIỂM TRA CÁC LỖI KHÔNG HIỆN TRÊN CONSOLE.**

**KHÔNG TUYÊN BỐ HOÀN THÀNH CHỈ VÌ GAME CHẠY ĐƯỢC.**

**CHỈ COI LÀ HOÀN THÀNH KHI HỆ THỐNG ĐÃ ĐƯỢC XÁC MINH Ở MỨC CAO NHẤT MÀ TOOLING VÀ THỜI GIAN CHO PHÉP.**

**TỰ CHỦ ĐỘNG BỔ SUNG NHỮNG GÌ CẦN THIẾT ĐỂ GAME ĐẠT CHẤT LƯỢNG CAO HƠN.**

**ĐỪNG CHỜ TÔI PHẢI NÓI TỪNG CHI TIẾT.**

**HÃY HÀNH ĐỘNG NHƯ MỘT GAME DIRECTOR + LEAD ENGINEER + QA LEAD THỰC THỤ.**

**MỤC TIÊU CUỐI CÙNG: MỘT GAME WEB VOXEL SANDBOX LỚN, ĐẸP, MƯỢT, SÂU, ỔN ĐỊNH VÀ THỰC SỰ ĐÁNG CHƠI.**
