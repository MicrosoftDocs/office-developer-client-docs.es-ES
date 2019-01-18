---
title: Name (propiedad, ADO)
TOCTitle: Name property (ADO)
ms:assetid: 4b19bd08-ac3c-86f0-471d-06a37a0d4f89
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249234(v=office.15)
ms:contentKeyID: 48544683
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f6fbfbd7008919cc4d784a4d0468d8471d102708
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721550"
---
# <a name="name-property-ado"></a>Name (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el nombre de un objeto.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String** que indica el nombre de un objeto.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Name** para asignar un nombre a un objeto **Command**, **Property**, **Field** o **Parameter** o para recuperar el nombre de cualquiera de éstos.

El valor es de lectura y escritura en un objeto **Command** y de sólo lectura en un objeto **Property**.

En un objeto **Field**, **Name** suele ser de sólo lectura. Sin embargo, en los nuevos objetos **Field** anexados a la colección [Fields](fields-collection-ado.md) de un objeto [Record](record-object-ado.md), **Name** es de lectura y escritura sólo después de haber especificado la propiedad [Value](value-property-ado.md) de **Field** y de haber agregado correctamente el proveedor de datos al nuevo objeto **Field** al llamar al método [Update](update-method-ado.md) de la colección **Fields**.

En los objetos **Parameter** que aún no se han anexado a la colección [Parameters](parameters-collection-ado.md), la propiedad **Name** es de lectura y escritura. En los objetos **Parameter** anexados y en el resto de los objetos, la propiedad **Name** es de sólo lectura. En una colección, los nombres no tienen que ser exclusivos.

Es posible recuperar la propiedad **Name** de un objeto mediante un número ordinal, tras lo cual se puede hacer referencia al objeto directamente por su nombre. Por ejemplo, si rstMain.Properties (20). Name produce Updatability, sucesivo puede hacer referencia a esta propiedad como produce Updatability, sucesivo puede hacer referencia a esta propiedad como rstMain.Properties("Updatability").

