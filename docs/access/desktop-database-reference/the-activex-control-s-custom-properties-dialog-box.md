---
title: Cuadro de diálogo de propiedades personalizadas del Control ActiveX
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485335"
---
# <a name="activex-controls-custom-properties-dialog-box"></a>Cuadro de diálogo de propiedades personalizadas del Control ActiveX

**Se aplica a**: Access 2013 | Office 2013

Al establecer las propiedades de un control ActiveX, puede necesitar o preferir el uso del cuadro de diálogo de propiedades personalizadas del control. Este cuadro de diálogo de propiedades personalizadas ofrece una alternativa a la lista de propiedades de la hoja de propiedades de Microsoft Access para establecer las propiedades del control ActiveX en la vista Diseño.

> [!NOTE]
> [!NOTA] Esta información sólo tiene aplicación para controles ActiveX en el entorno de una base de datos de Microsoft Access.



## <a name="two-ways-to-set-properties"></a>Dos modos de establecer las propiedades

La razón de ser del cuadro de diálogo de propiedades personalizadas es que no todas las aplicaciones que usan controles ActiveX ofrecen una hoja de propiedades como la de Microsoft Access. El cuadro de diálogo de propiedades personalizadas ofrece una interfaz para establecer las propiedades clave del control sea cual sea la interfaz suministrada por la aplicación.

Para algunas propiedades de los controles ActiveX, es posible elegir establecer las propiedades en:

  - La hoja de propiedades de Microsoft Access.

  - El cuadro de diálogo de propiedades personalizadas del control ActiveX.

En algunos casos, el cuadro de diálogo de propiedades personalizadas es el único medio disponible para establecer una propiedad en la vista Diseño. Ésta es normalmente la situación cuando la interfaz necesaria para establecer una propiedad no funciona dentro de la hoja de propiedades de Microsoft Access. Por ejemplo, la propiedad **FuenteDeCuadrícula (GridFont)** del control Calendar tiene varios argumentos; no es posible establecer más de un argumento para cada propiedad en la hoja de propiedades de Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Localizar el Cuadro de diálogo de propiedades personalizadas

No todos los controles ActiveX ofrecen un cuadro de diálogo de propiedades personalizadas. Para ver si un control ofrece este cuadro de diálogo de propiedades personalizadas, busque la propiedad **Personalizado (Custom)** en la hoja de propiedades de Microsoft Access para este control. Si la lista de propiedades incluye **Personalizado**, entonces el control dispone de cuadro de diálogo de propiedades personalizadas.

## <a name="using-the-custom-properties-dialog-box"></a>Utilización del Cuadro de diálogo de propiedades personalizadas

Después de hacer clic en el cuadro de la propiedad **Personalizado** en la hoja de propiedades de Microsoft Access, haga clic en el botón **Generar** situado a la derecha del cuadro de la propiedad para mostrar el cuadro de diálogo de propiedades personalizadas del control, a menudo presentada en forma de cuadro de diálogo con fichas. Seleccione la ficha que contenga la interfaz para las propiedades que desee establecer.

Después de realizar cambios en una ficha, normalmente se pueden aplicar dichos cambios inmediatamente haciendo clic en el botón **Aplicar** (si está presente). Puede hacer clic en otras pestañas para establecer otras propiedades según sus necesidades. Para confirmar todos los cambios en el cuadro de diálogo de propiedades personalizadas, haga clic en el botón **Aceptar**. Para volver a la hoja de propiedades de Microsoft Access sin cambiar los valores de ninguna propiedad, haga clic en el botón **Cancelar**.

También puede ver el cuadro de diálogo de propiedades personalizadas haciendo clic en el subcomando **Propiedades** del comando **Objeto** del control ActiveX (por ejemplo, **Objeto Control de calendario**) del menú **Edición**, o haciendo clic en este mismo subcomando en el menú contextual del control ActiveX. Además, algunas propiedades de la hoja de propiedades de Microsoft Access para el control ActiveX, como la propiedad **GridFontColor** del control Calendar, disponen de un botón **Generar** situado a la derecha del cuadro de la propiedad. Al hacer clic en el botón **Generar**, se muestra el cuadro de diálogo de propiedades personalizadas, con la ficha correspondiente ya seleccionada (por ejemplo, **Colores**).

