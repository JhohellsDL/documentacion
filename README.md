# Documentación de RideBadge

## Descripción General
`RideBadge` es un componente personalizado de Android que muestra una insignia con texto, ícono y estilos personalizables. Admite varios atributos para ajustar su apariencia y comportamiento, lo que lo hace versátil para diferentes casos de uso, como insignias promocionales o de descuento.

## Características
- Muestra un distintivo con texto y un icono opcional.
- Personaliza el texto del distintivo, el color del texto, el color de fondo y la visibilidad del icono.
- Elige entre diferentes estilos de distintivo: Descuento y Promocional.

## Atributos

| Atributo                     | Formato   | Descripción                                                                    |
|------------------------------|-----------|--------------------------------------------------------------------------------|
| `rs_text_badge`              | `string`  | El texto que se muestra dentro de la insignia.                                 |
| `rs_textColor_badge`         | `string`  | El color del texto que se muestra dentro de la insignia.                        |
| `rs_iconColor_badge`         | `string`  | El color del ícono que se muestra dentro de la insignia.                        |
| `rs_visibility_badge`        | `boolean` | La visibilidad de la insignia (true para visible, false para invisible).        |
| `rs_visibilityIcon_badge`    | `boolean` | La visibilidad del ícono dentro de la insignia (true para visible, false para invisible). |
| `rs_backgroundColor_badge`   | `string`  | El color de fondo de la insignia.                                               |
| `rs_style_badge`             | `enum`    | El estilo de la insignia, ya sea `discount` o `promotional`.                    |
| `rs_icon_src_badge`          | `reference`| El recurso drawable para el ícono que se muestra dentro de la insignia.         |
| `rs_textStyle_badge`         | `reference`| El estilo aplicado al texto dentro de la insignia.                              |

## Estilos
El atributo `rs_style_badge` puede configurarse con uno de los siguientes valores:

- `discount` (valor: 0)
- `promotional` (valor: 1)

## Uso
A continuación se presentan ejemplos de cómo usar el componente `RideBadge` en tus archivos XML de diseño:

### Ejemplo 1: Insignia Simple
```xml
<com.rimac.components.views.badges.RideBadge
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    app:rs_text_badge="20% OFF"
    app:rs_textColor_badge="#FF0000"
    app:rs_backgroundColor_badge="#00FF00"
    app:rs_visibility_badge="true"
    app:rs_visibilityIcon_badge="true"
    app:rs_style_badge="discount"
    app:rs_icon_src_badge="@drawable/custom_icon"
    app:rs_textStyle_badge="@style/ride_sys_text_label_small_default"/>
