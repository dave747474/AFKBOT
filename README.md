  bot.on('physicTick', () => {
    if (bot.pvp.target) return
    if (bot.pathfinder.isMoving()) return

    const entity = bot.nearestEntity()
    if (entity) bot.lookAt(entity.position.offset(0, entity.height, 0))
  })
  bot.on('physicTick', () => {
    if (!guardPos) return
    const filter = e => e.type === 'mob' && e.position.distanceTo(bot.entity.position) < 16 &&
      e.mobType !== 'Armor Stand'
    const entity = bot.nearestEntity(filter)
    if (entity) {
      bot.pvp.attack(entity)
    }
  })
  bot.on('chat', (username, message) in =bot.on('physicTick', () => {
    if (bot.pvp.target) return
    if (bot.pathfinder.isMoving()) return

    const entity = bot.nearestEntity()
    if (entity) bot.lookAt(entity.position.offset(0, entity.height, 0))
  })
  bot.on('physicTick', () => {
    if (!guardPos) return
    const filter = e => e.type === 'mob' && e.position.distanceTo(bot.entity.position) < 16 &&
      e.mobType !== 'Armor Stand'
    const entity = bot.nearestEntity(filter)
    if (entity) {
      bot.pvp.attack(entity)
    }
  })
  bot.on('chat', (username, message) => {> {
