---
title: Propiedad Name (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288661"
---
# <a name="name-property-ado-md"></a>Propiedad Name (ADO MD)


**Se aplica a:** Access 2013, Office 2013

Indica el nombre de un objeto.

## <a name="return-values"></a>Valores devueltos

Devuelve un valor **String** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

Puede recuperar la propiedad **Name** de un objeto mediante una referencia ordinal, después de la cual, puede hacer referencia al objeto directamente por el nombre. Por ejemplo, si cdf.CubeDefs(0).Name devuelve "Videoclub Bobs", puede hacer referencia a este [CubeDef](cubedef-object-ado-md.md) como cdf.CubeDefs("Videoclub Bobs").

