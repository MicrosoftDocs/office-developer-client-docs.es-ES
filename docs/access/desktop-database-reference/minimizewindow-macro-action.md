---
title: MinimizarVentana (acción de macro)
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9f7c4ab535010dc0329673fd04721615f6eb3cd8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288886"
---
# <a name="minimizewindow-macro-action"></a>MinimizarVentana (acción de macro)

**Se aplica a:** Access 2013, Office 2013

Si Access está configurado para usar ventanas superpuestas en lugar de documentos con pestañas, puedes usar la acción **MinimizarVentana** para reducir la ventana activa a una pequeña barra de título en la parte inferior de la ventana de Access.

> [!NOTE]
> [!NOTA] Esta acción no puede aplicarse a las ventanas de código en el Editor de Visual Basic. Para obtener información sobre cómo afectar a las ventanas de código, vea el tema de la propiedad **WindowState**.

## <a name="setting"></a>Configuración

La acción **MinimizarVentana** no tiene argumentos.

## <a name="remarks"></a>Comentarios

Puede usar esta acción para quitar una ventana de la pantalla sin cerrar el objeto. También puede utilizarla para abrir un objeto sin mostrar su ventana. Para mostrar el objeto, utilice la acción **SeleccionarObjeto** con la acción **MaximizarVentana** o **RestaurarVentana**. La acción **RestaurarVentana** restaura el tamaño anterior de una ventana minimizada.

La acción **MinimizarVentana** tiene el mismo efecto que hacer clic en el botón **Minimizar** situado en la esquina superior derecha de la ventana o hacer clic en **Minimizar** en el menú **Control** de la ventana.

**Sugerencias**

- Si la ventana que desea minimizar no es la ventana activa, puede que primero sea necesario utilizar la acción **SeleccionarObjeto**.

- Para ocultar el panel de navegación, utilice la acción **SeleccionarObjeto** con el valor del argumento En panel de navegación establecido en **Sí** y, a continuación, utilice la acción **MinimizarVentana**. El objeto que seleccione con la acción **SeleccionarObjeto** puede ser cualquiera de la base de datos.

- Puede ocultar la ventana activa, haciendo clic en **Administrar esta ventana** en el menú **Ver** y, a continuación, en **Ocultar**. En lugar de reducirse a un icono, la ventana deja de estar visible. Utilice el comando **Mostrar** del mismo menú para que vuelva a aparecer la ventana. Puede usar la acción **EjecutarComandoDeMenú** para ejecutar cualquiera de estos comandos desde una macro.

- También puede utilizar la acción **EstablecerValor** para establecer el valor de la propiedad **Visible** de un formulario de manera que se oculte o se muestre su ventana.

Para ejecutar la acción **MinimizarVentana** en un módulo de Visual Basic para Aplicaciones (VBA), use el método **Minimize** del objeto **DoCmd**.

