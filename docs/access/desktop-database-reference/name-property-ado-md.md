---
title: Name (propiedad, ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cc7a89e0d6b9cdaed2c54d3269b61280ce3306c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25484121"
---
# <a name="name-property-ado-md"></a>Name (propiedad, ADO MD)


**Se aplica a**: Access 2013 | Office 2013

Indica el nombre de un objeto.

## <a name="return-values"></a>Valores devueltos

Devuelve un valor **String** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

Puede recuperar la propiedad **Name** de un objeto mediante una referencia ordinal, después de la cual, puede hacer referencia al objeto directamente por el nombre. Por ejemplo, si cdf.CubeDefs(0).Name devuelve "Videoclub Bobs", puede hacer referencia a este [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Videoclub Bobs").

