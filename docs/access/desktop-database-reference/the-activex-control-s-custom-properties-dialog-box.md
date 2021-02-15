---
title: Cuadro de diálogo Propiedades personalizadas de un control ActiveX
TOCTitle: ActiveX control custom properties dialog box
description: Este cuadro de diálogo de propiedades personalizadas ofrece una alternativa a la lista de propiedades de la hoja de propiedades de Microsoft Access para establecer las propiedades del control ActiveX en la vista Diseño.
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4574abc86e6eacd38721e601d26c8b8fbf0a0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314109"
---
# <a name="activex-control-custom-properties-dialog-box"></a>Cuadro de diálogo Propiedades personalizadas de un control ActiveX

**Se aplica a:** Access 2013, Office 2013

Al establecer las propiedades de un control ActiveX, puede necesitar o preferir el uso del cuadro de diálogo de propiedades personalizadas del control. Este cuadro de diálogo de propiedades personalizadas ofrece una alternativa a la lista de propiedades de la hoja de propiedades de Microsoft Access para establecer las propiedades del control ActiveX en la vista Diseño.

> [!NOTE]
> [!NOTA] Esta información sólo tiene aplicación para controles ActiveX en el entorno de una base de datos de Microsoft Access.

## <a name="two-ways-to-set-properties"></a>Dos formas de establecer propiedades

La razón de ser del cuadro de diálogo de propiedades personalizadas es que no todas las aplicaciones que usan controles ActiveX ofrecen una hoja de propiedades como la de Microsoft Access. El cuadro de diálogo de propiedades personalizadas ofrece una interfaz para establecer las propiedades clave del control sea cual sea la interfaz suministrada por la aplicación.

Para algunas propiedades de los controles ActiveX, es posible elegir establecer las propiedades en:

- La hoja de propiedades de Microsoft Access.
- El cuadro de diálogo de propiedades personalizadas del control ActiveX.

En algunos casos, el cuadro de diálogo de propiedades personalizadas es el único medio disponible para establecer una propiedad en la vista Diseño. Ésta es normalmente la situación cuando la interfaz necesaria para establecer una propiedad no funciona dentro de la hoja de propiedades de Microsoft Access. Por ejemplo, la propiedad **FuenteDeCuadrícula (GridFont)** del control Calendar tiene varios argumentos; no es posible establecer más de un argumento para cada propiedad en la hoja de propiedades de Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Buscar el cuadro de diálogo de propiedades personalizadas

No todos los controles ActiveX ofrecen un cuadro de diálogo de propiedades personalizadas. Para ver si un control ofrece este cuadro de diálogo de propiedades personalizadas, busque la propiedad **Personalizado (Custom)** en la hoja de propiedades de Microsoft Access para este control. Si la lista de propiedades contiene el nombre **Personalizado**, el control proporciona el cuadro de diálogo de propiedades personalizadas.

## <a name="using-the-custom-properties-dialog-box"></a>Uso del cuadro de diálogo de propiedades personalizadas

Después de  elegir el cuadro de propiedades personalizadas  en la hoja de propiedades de Microsoft Access, elija el botón Generar a la derecha del cuadro de propiedades para mostrar el cuadro de diálogo de propiedades personalizadas del control, que a menudo se presenta como un cuadro de diálogo con fichas. Seleccione la ficha que contenga la interfaz para establecer las propiedades deseadas.

Después de realizar cambios en una pestaña, a menudo puede aplicar esos cambios inmediatamente seleccionando el botón **Aplicar** (si se proporciona). Puede elegir otras pestañas para establecer otras propiedades según sea necesario. Para aprobar todos los cambios realizados en el cuadro de diálogo de propiedades personalizadas, elija el **botón** Aceptar. Para volver a la hoja de propiedades de Microsoft Access sin cambiar la configuración de propiedades, elija el **botón** Cancelar.

También puede ver el cuadro de diálogo de propiedades personalizadas seleccionando  el **subcomando** Propiedades del comando  objeto del control ActiveX (por ejemplo, Objeto de **control** de calendario) en el menú Edición, o eligiendo este mismo subcomando en el menú contextual del control ActiveX. Además, algunas propiedades de la hoja de propiedades de Microsoft Access para el control ActiveX, como la propiedad **ColorDeFuenteDeCuadrícula (GridFontColor)** del control Calendar, disponen de un botón **Generar** a la derecha del cuadro de la propiedad. Al elegir el botón **Generar,** se muestra el cuadro de diálogo de propiedades personalizadas, con la ficha adecuada seleccionada (por ejemplo, **Colores).**

