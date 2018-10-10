---
title: CommandType (propiedad, ADO)
TOCTitle: CommandType Property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3cff3c3540208b142fc13cd79eb83bd218814873
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486798"
---
# <a name="commandtype-property-ado"></a>CommandType (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica el tipo de un objeto [Command](command-object-ado.md).

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve uno o varios valores de [CommandTypeEnum](commandtypeenum.md).


> [!NOTE]
> <P>[!NOTA] No use los valores <STRONG>adCmdFile</STRONG> ni <STRONG>adCmdTableDirect</STRONG> de <STRONG>CommandTypeEnum</STRONG> con la propiedad <STRONG>CommandType</STRONG>. Estos valores se pueden usar únicamente como opciones con los métodos <A href="open-method-ado-recordset.md">Open</A> y <A href="requery-method-ado.md">Requery</A> de un objeto <A href="recordset-object-ado.md">Recordset</A>.</P>



## <a name="remarks"></a>Comentarios

Utilice la propiedad **CommandType** para optimizar la evaluación de la propiedad [CommandText](commandtext-property-ado.md).

Si el valor de la propiedad **CommandType** es **adCmdUnknown** (el valor predeterminado), puede que disminuya el rendimiento porque ADO debe realizar llamadas al proveedor para determinar si la propiedad **CommandText** es una instrucción SQL, un procedimiento almacenado o un nombre de tabla. Si se conoce el tipo de comando que se está usando y se establece el valor de la propiedad **CommandType**, se indica a ADO que vaya directamente al código pertinente. Si el valor de la propiedad **CommandType** no coincide con el tipo de comando especificado por la propiedad **CommandText**, se genera un error cuando se llama al método [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).

