---
title: Direction (propiedad, ADO)
TOCTitle: Direction Property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611e5efbe53964c5ba255380e2659f024bd6be9a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485305"
---
# <a name="direction-property-ado"></a>Direction (propiedad, ADO)


**Se aplica a**: Access 2013 | Office 2013

Indica si [Parameter](parameter-object-ado.md) representa un parámetro de entrada, de salida, de entrada y salida o si es el valor devuelto por un procedimiento almacenado.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo [ParameterDirectionEnum](parameterdirectionenum.md).

## <a name="remarks"></a>Comentarios

Use la propiedad **Direction** para especificar cómo pasa un parámetro a un procedimiento o desde este. La propiedad **Direction** es de lectura y escritura, lo que le permite trabajar con proveedores que no devuelven dicha información o establecerla cuando no se desea que ADO realice una llamada adicional al proveedor para recuperar información del parámetro.

No todos los proveedores pueden determinar la dirección de los parámetros de los procedimientos almacenados. En estos casos, es necesario establecer la propiedad **Direction** antes de ejecutar la consulta.

