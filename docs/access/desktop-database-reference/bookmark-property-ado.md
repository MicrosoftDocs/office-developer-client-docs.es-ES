---
title: Propiedad Bookmark (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 17818fe2b4f826cbcfbbb3955817c2b5d99ab6a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296797"
---
# <a name="bookmark-property-ado"></a>Propiedad Bookmark (ADO)


**Se aplica a:** Access 2013, Office 2013

Indica un marcador que identifica de manera única el registro actual de un objeto [Recordset](recordset-object-ado.md) o que establece el registro actual de un objeto **Recordset** en el registro identificado por un marcador válido.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve una expresión de tipo **Variant** que da como resultado un marcador válido.

## <a name="remarks"></a>Comentarios

Utilice la propiedad **Bookmark** para guardar la posición del actual registro y volver al mismo más adelante. Los marcadores sólo están disponibles en los objetos **Recordset** que admitan la funcionalidad de los marcadores.

Al abrirse un objeto **Recordset**, cada uno de sus registros tiene un marcador único. Para guardar el marcador del registro actual, asigne el valor de la propiedad **Bookmark** a una variable. Para poder volver rápidamente a ese registro después de moverse a otro, establezca la propiedad **Bookmark** del objeto **Recordset** en el valor de dicha variable.

Puede que el usuario no vea el valor del marcador. Además, los marcadores no son necesariamente comparables de manera directa: dos marcadores que hacen referencia al mismo registro pueden tener valores diferentes.

Si se utiliza el método [Clone](clone-method-ado.md) para crear una copia de un objeto **Recordset**, los valores de configuración de la propiedad **Bookmark** de los objetos **Recordset** original y duplicado son idénticos y se pueden utilizar de manera intercambiable. Sin embargo, no se pueden utilizar de manera intercambiable los marcadores de diferentes objetos **Recordset**, incluso si se crearon a partir del mismo origen o comando.

**Uso del servicio de datos remotos** Cuando se usa en un objeto **Recordset del** lado cliente, la **propiedad Bookmark** siempre está disponible.

