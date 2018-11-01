---
title: CommandType (propiedad, ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 89264889281070b8a477c3a04b8f6f5735efdf3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880239"
---
# <a name="commandtype-property-ado"></a>CommandType (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el tipo de un objeto [Command](command-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve uno o varios valores de [CommandTypeEnum](commandtypeenum.md).

> [!NOTE]
> [!NOTA] No use los valores **adCmdFile** ni **adCmdTableDirect** de **CommandTypeEnum** con la propiedad **CommandType**. Estos valores se pueden usar únicamente como opciones con los métodos [Open](open-method-ado-recordset.md) y [Requery](requery-method-ado.md) de un objeto [Recordset](recordset-object-ado.md).


## <a name="remarks"></a>Comentarios

Utilice la propiedad **CommandType** para optimizar la evaluación de la propiedad [CommandText](commandtext-property-ado.md).

Si el valor de la propiedad **CommandType** es **adCmdUnknown** (el valor predeterminado), puede que disminuya el rendimiento porque ADO debe realizar llamadas al proveedor para determinar si la propiedad **CommandText** es una instrucción SQL, un procedimiento almacenado o un nombre de tabla. Si se conoce el tipo de comando que se está usando y se establece el valor de la propiedad **CommandType**, se indica a ADO que vaya directamente al código pertinente. Si el valor de la propiedad **CommandType** no coincide con el tipo de comando especificado por la propiedad **CommandText**, se genera un error cuando se llama al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).

