## __Logachev Gleb__
## Contact Info
[![Telegram](https://img.shields.io/badge/-telegram-151414?style=for-the-badge&logo=telegram)](https://t.me/Gllog)
[![Vkontakte](https://img.shields.io/badge/-VK-151414?style=for-the-badge&logo=vk)](https://vk.com/g_logachev)
[![github](https://img.shields.io/badge/-github-090909?style=for-the-badge&logo=github)](https://github.com/GlebLogachev)

## Summary
### i am a junior android developer. I am constantly learning something new, I want to get better every day. that's why I'm here

## Skills
![Android](https://img.shields.io/badge/-ANDROID-090909?style=for-the-badge&logo=android)
![Kotlin](https://img.shields.io/badge/-KOTLIN-090909?style=for-the-badge&logo=kotlin)
![Git](https://img.shields.io/badge/-Git-090909?style=for-the-badge&logo=git)
![MVP/MVVM](https://img.shields.io/badge/-MVP/MVVM-090909?style=for-the-badge)
![Rxjava](https://img.shields.io/badge/-RXJAVA-090909?style=for-the-badge&logo=reactivex&logoColor=ff5bff)
![Coroutines](https://img.shields.io/badge/-COROUTINES-090909?style=for-the-badge)
![Dagger](https://img.shields.io/badge/-Dagger-090909?style=for-the-badge)
![Retrofit](https://img.shields.io/badge/-RETROFIT-090909?style=for-the-badge&logo=dugger)
![Clean Architecture](https://img.shields.io/badge/-CLEAN_ARCHITECTURE-090909?style=for-the-badge)

## Experience
### 1. Siberian.pro 1, 2021 - present
### Junior android developer

### 2. "Make" 8, 2020 - 12, 2020
### Mobile developer (React native)

## Education
__Kemerovo State University__<br>
__Direction__: Economics
## English lvl
### __B1__

## Code examples
>### e.g my last DB query :)

```
class CatalogInteractor @Inject constructor(
    private val database: AppDatabase
) {

    fun getProductDetails(product_id: Long) =
        Single.zip(getProduct(product_id), getVideos(product_id),
            { product, video ->
                product to video
            })

    private fun getProduct(id: Long): Single<ProductDomain> {
        return database
            .productDao()
            .find(id = id)
            .map {
                it.toDomain()
            }
    }

    private fun getVideos(id: Long): Single<List<Video>> {
        return database
            .videosDao()
            .getVideos(id)
            .map { list ->
                list.map {
                    it.toModel
                }
            }
    }
 }
  ```