---
title: Children (propiedad, ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e126b203e2282f96070f1f3eb14a9b926c04f432
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483906"
---
# <a name="children-property-ado-md"></a>Children (propiedad, ADO MD)


**Se aplica a**: Access 2013 | Office 2013

Devuelve una colección [Members](members-collection-ado-md.md) para la que el [elemento](member-object-ado-md.md) activo es el principal en la jerarquía.

## <a name="return-values"></a>Valores devueltos

Devuelve una colección **Members** y es de sólo lectura.

## <a name="remarks"></a>Comentarios

La propiedad **Children** contiene una colección **Members** para la que el **elemento** activo es el principal de la jerarquía. Los objetos **Member** del nivel de hoja no tienen elementos secundarios en la colección **Members**. Esta propiedad solo es compatible con objetos **Member** pertenecientes a un objeto [Level](level-object-ado-md.md). Si se hace referencia a esta propiedad desde objetos **Member** pertenecientes a un objeto [Position](position-object-ado-md.md), se produce un error.

