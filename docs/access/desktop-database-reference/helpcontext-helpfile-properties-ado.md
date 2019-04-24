---
title: Propiedades ContextoDeAyuda (HelpContext), HelpFile (ADO)
TOCTitle: HelpContext, HelpFile properties (ADO)
ms:assetid: 8a79f994-f17c-2983-0593-095801be762e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249608(v=office.15)
ms:contentKeyID: 48546194
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c90fee6b8525ab13c8a294f9b39c52c20f580a62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291995"
---
# <a name="helpcontext-helpfile-properties-ado"></a>Propiedades ContextoDeAyuda (HelpContext), HelpFile (ADO)

**Se aplica a:** Access 2013, Office 2013

Indican el archivo de Ayuda y el tema asociados a un objeto [Error](error-object-ado.md).

## <a name="return-values"></a>Valores devueltos

- **HelpContextID**: devuelve un identificador de contexto, como un valor de tipo **Long**, de un tema de un archivo de Ayuda.

- **HelpFile**: devuelve un valor de tipo **String** que evalúa una ruta de acceso completa resuelta a un archivo de Ayuda.

## <a name="remarks"></a>Comentarios

Si se especifica un archivo de Ayuda en la propiedad **HelpFile**, la propiedad **ContextoDeAyuda (HelpContext)** se utiliza para mostrar automáticamente el tema de Ayuda que identifica. Si no hay ningún tema de Ayuda pertinente disponible, la propiedad **ContextoDeAyuda (HelpContext)** devuelve cero y la propiedad **HelpFile** devuelve una cadena de longitud cero ("").

