---
title: Propiedad Prepared (ADO)
TOCTitle: Prepared property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9541b2d584728c09ee852f628cdfc35f3d170f04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301459"
---
# <a name="prepared-property-ado"></a>Propiedad Prepared (ADO)


**Se aplica a:** Access 2013, Office 2013

Indica si se va a guardar una versión compilada de un comando antes de la ejecución.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Boolean** que, si se establece en **True**, indica que debe prepararse el comando.

## <a name="remarks"></a>Comentarios

Use la propiedad **Prepared** para que el proveedor guarde una versión preparada (o compilada) de la consulta especificada en la propiedad [CommandText](commandtext-property-ado.md) antes de la primera ejecución de un objeto [Command](command-object-ado.md). Esto puede ralentizar la primera ejecución de un comando, pero una vez que el proveedor lo compila, usará la versión compilada del comando para todas las ejecuciones siguientes, lo que dará lugar a una mejora del rendimiento.

Si la propiedad es **False**, el proveedor ejecutará el objeto **Command** directamente sin crear una versión compilada.

Si el proveedor no admite la preparación del comando, puede devolver un error en cuanto esta propiedad se establezca en **True**. Si no devuelve un error, simplemente omite la solicitud de preparar el comando y establece la propiedad **Prepared** en **False**.

