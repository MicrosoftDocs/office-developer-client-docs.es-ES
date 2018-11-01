---
title: Prepared (propiedad, ADO)
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
ms.openlocfilehash: a9c275cfe16ac2f1b1f9d2a8c0ac857010ed4572
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878755"
---
# <a name="prepared-property-ado"></a>Prepared (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica si se va a guardar una versión compilada de un comando antes de la ejecución.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **Boolean** que, si se establece en **True**, indica que debe prepararse el comando.

## <a name="remarks"></a>Comentarios

Use la propiedad **Prepared** para que el proveedor guarde una versión preparada (o compilada) de la consulta especificada en la propiedad [CommandText](commandtext-property-ado.md) antes de la primera ejecución de un objeto [Command](command-object-ado.md). Esto puede ralentizar la primera ejecución de un comando, pero una vez que el proveedor lo compila, usará la versión compilada del comando para todas las ejecuciones siguientes, lo que dará lugar a una mejora del rendimiento.

Si la propiedad es **False**, el proveedor ejecutará el objeto **Command** directamente sin crear una versión compilada.

Si el proveedor no admite la preparación del comando, puede devolver un error en cuanto esta propiedad se establezca en **True**. Si no devuelve un error, simplemente omite la solicitud de preparar el comando y establece la propiedad **Prepared** en **False**.

