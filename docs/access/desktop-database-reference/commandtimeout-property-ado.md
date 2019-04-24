---
title: CommandTimeout (propiedad, ADO)
TOCTitle: CommandTimeout property (ADO)
ms:assetid: a0b6209c-9feb-08ae-002a-15d1d20734a8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249739(v=office.15)
ms:contentKeyID: 48546714
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231124
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9d44bc8fae0143b183ef54120cdaaf91337f36f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296132"
---
# <a name="commandtimeout-property-ado"></a>CommandTimeout (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el tiempo que se va a esperar durante la ejecución de un comando para que finalice el intento y se genere un error.

## <a name="settings-and-return-values"></a>Valores de configuración y devueltos

Establece o devuelve un valor de tipo **Long** que indica, en segundos, cuánto tiempo se va a esperar a que se ejecute un comando. El valor predeterminado es 30.

## <a name="remarks"></a>Comentarios

Use la propiedad **CommandTimeout** de un objeto [Connection](connection-object-ado.md) o un objeto [Command](command-object-ado.md) para permitir la cancelación de una llamada al método [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) debido a una demora en el tráfico de red o a la sobrecarga del servidor. Si el intervalo establecido en la propiedad **CommandTimeout** transcurre antes de que finalice la ejecución del comando, se genera un error y ADO cancela el comando. Si se establece el valor de la propiedad en cero, ADO esperará indefinidamente a que finalice la ejecución. Asegúrese de que el proveedor y el origen de datos en el que está escribiendo código admiten la funcionalidad **CommandTimeout**.

La configuración de **CommandTimeout** en un objeto **Connection** no afecta a la configuración de **CommandTimeout** en un objeto **Command** del mismo objeto **Connection**; es decir, la propiedad **CommandTimeout** del objeto **Command** no hereda el valor de la propiedad **CommandTimeout** del objeto **Connection**.

En un objeto **Connection**, la propiedad **CommandTimeout** sigue siendo de lectura y escritura después de abrirse el objeto **Connection**.

