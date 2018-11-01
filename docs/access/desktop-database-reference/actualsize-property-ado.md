---
title: ActualSize (propiedad, ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
ms.openlocfilehash: 627f4fe93340c69b62f81c1b10ebf231938eea89
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873190"
---
# <a name="actualsize-property-ado"></a>ActualSize (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Indica la longitud real del valor de un campo.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Devuelve un valor de tipo **Long**. Algunos proveedores pueden permitir la configuración de esta propiedad para reservar espacio para datos BLOB, en cuyo caso el valor predeterminado es 0.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **ActualSize** para devolver la longitud real del valor de un objeto [Field](field-object-ado.md). La propiedad **ActualSize** es de sólo lectura para todos los campos. Si ADO no puede determinar la longitud del valor del objeto **Field**, la propiedad **ActualSize** devuelve **adUnknown**.

Las propiedades **ActualSize** y [DefinedSize](definedsize-property-ado.md) son diferentes. Un objeto **Field** con un tipo declarado de **adVarChar** y una longitud máxima de 50 caracteres devuelve 50 como valor de la propiedad **DefinedSize**, pero el valor que se devuelve para la propiedad **ActualSize** es la longitud de los datos almacenados en el campo del registro actual. Los objetos **Field** con un valor de **DefinedSize** mayor que 255 bytes se tratan como columnas de longitud variable.

