---
title: DefinedSize (propiedad, ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a0e67cfdbe60ebf2c49cb3e726311d2fa61bd3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868857"
---
# <a name="definedsize-property-ado"></a>DefinedSize (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica la capacidad de datos de un objeto [Field](field-object-ado.md).

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de tipo **Long** que refleja el tamaño definido de un campo como un número de bytes.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **DefinedSize** para determinar la capacidad de datos de un objeto **Field**.

Las propiedades **DefinedSize** y [ActualSize](actualsize-property-ado.md) son diferentes. Por ejemplo, considere un objeto **Field** con un tipo declarado **adVarChar** y un valor de la propiedad **DefinedSize** de 50 que contenga un carácter único. El valor de la propiedad **ActualSize** que devuelve es la longitud del carácter único en bytes.

