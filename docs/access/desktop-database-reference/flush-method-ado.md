---
title: 'Flush (método): ActiveX data objects (ADO)'
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a55eb66c454d510d53083c495326548eda08af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292345"
---
# <a name="flush-method-ado"></a>Método Flush (ADO)


**Se aplica a:** Access 2013, Office 2013

Vuelca el contenido del objeto [Stream](stream-object-ado.md) que queda en el búfer de ADO en el objeto subyacente al que está asociado el objeto **Stream**.

## <a name="syntax"></a>Sintaxis

*Stream*. Vaciado

## <a name="remarks"></a>Comentarios

Este método puede utilizarse para enviar el contenido del búfer de secuencia al objeto subyacente (por ejemplo, el nodo o archivo representado por la dirección URL que es el origen del objeto **Stream** ). Este método debe invocarse cuando se desea garantizar que se hayan escrito todos los cambios realizados en el contenido de un objeto **Stream**. Sin embargo, con ADO, normalmente no es necesario llamar a **Flush**, puesto que ADO vacía continuamente y en la medida de lo posible su búfer en segundo plano. Los cambios en el contenido de un objeto **Stream** se realizan automáticamente y no se almacenan en la memoria caché hasta que se llama al método **Flush**.

Si se cierra un objeto **Stream** con el método [Close](close-method-ado.md), se vacía automáticamente el contenido del objeto **Stream**; no es necesario llamar explícitamente a **Flush** inmediatamente antes de llamar a **Close**.

