# Game Animation Sample
A third-person melee prototype built in Unreal Engine 5, featuring modular weapons, precise hit detection, stamina/poise systems, directional knockback with hit-stun, resettable light/heavy combo chains, 8-way rolls/backstep/guard, enemy lock-on with target switching, and an animation stack that combines Motion Matching with layered blends for smooth, natural transitions and reduced “mechanical” feel.

## Weapons & Hit Detection
•	Modular BaseWeapon setup: socket-driven line/sphere traces for hits; applies damage + hit-stun + 4-direction knockback; montage-timed hitboxes.
•	Implemented ignore self/ignore list, multi-hit dedupe per swing, and debug visualization.

## Combat Loop
•	8-way rolls, backstep, guard with stamina/poise interaction; resettable light/heavy combos plus running/sprint/jump attacks.
•	Lock-on / unlock and target switching (left/right or mouse wheel), with camera and movement vectors aligned to the locked target.
•	Stamina/Poise costs and thresholds that gate actions and trigger stagger/knockdown states.

## Animation System
•	Integrated Motion Matching and combined it with Layered Blend per Bone / Animation Slots: upper-body attack montages while the lower body stays on MM-driven locomotion.
•	IK Retargeting for cross-skeleton reuse; direction-aware roll montage selection based on velocity/acceleration.

## Data & Architecture
•	Data-driven weapon/attack segments (damage, poise, timing); Enhanced Input mappings.
•	Tunables for trace radius/length, collision channels, lock-on selection (angle/distance/LOS), and camera offsets.
