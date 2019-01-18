---
title: ActualSize (propiedad, ADO)
TOCTitle: ActualSize property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 10/16/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c13cb41299ddaf786e6412e43a50b1414ad818b4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698207"
---
# <a name="actualsize-property-ado"></a>ActualSize (propiedad, ADO)

**Se aplica a**: Access 2013, Office 2013

Indica la longitud real del valor de un campo.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Devuelve un valor de tipo **Long**. Algunos proveedores pueden permitir la configuración de esta propiedad para reservar espacio para datos BLOB, en cuyo caso el valor predeterminado es 0.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **ActualSize** para devolver la longitud real del valor de un objeto [Field](field-object-ado.md). La propiedad **ActualSize** es de sólo lectura para todos los campos. Si ADO no puede determinar la longitud del valor del objeto **Field**, la propiedad **ActualSize** devuelve **adUnknown**.

Las propiedades **ActualSize** y [DefinedSize](definedsize-property-ado.md) son diferentes. Un objeto **Field** con un tipo declarado de **adVarChar** y una longitud máxima de 50 caracteres devuelve 50 como valor de la propiedad **DefinedSize**, pero el valor que se devuelve para la propiedad **ActualSize** es la longitud de los datos almacenados en el campo del registro actual. Los objetos **Field** con un valor de **DefinedSize** mayor que 255 bytes se tratan como columnas de longitud variable.

