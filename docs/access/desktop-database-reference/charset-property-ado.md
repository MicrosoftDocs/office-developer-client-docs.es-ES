---
title: Charset (propiedad, ADO)
TOCTitle: Charset property (ADO)
ms:assetid: 454f664e-6d62-eec9-487d-882c2f9503b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249213(v=office.15)
ms:contentKeyID: 48544551
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ca4640940c217fd81cac4ba1d8ffaf769b506fe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296391"
---
# <a name="charset-property-ado"></a>Charset (propiedad, ADO)


**Se aplica a:** Access 2013, Office 2013

Indica el juego de caracteres al que debe convertirse el contenido de un objeto [Stream](stream-object-ado.md) de texto para su almacenamiento en el búfer interno de objetos Stream.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String** que especifica el juego de caracteres al que se va a convertir el contenido del objeto **Stream**. El valor predeterminado es "Unicode". Los valores permitidos son cadenas típicas que se pasan a través de la interfaz como cadenas de juegos de caracteres de Internet (por ejemplo, "iso-8859-1", "Windows-1252", etc.). Para obtener una lista de las cadenas de juego de caracteres conocidas por un sistema, vea las subclaves de HKEY CLASSES ROOT MIME Database Charset en el Registro \_ \_ de \\ \\ \\ Windows.

## <a name="remarks"></a>Comentarios

En un objeto **Stream** de texto, los datos se almacenan en el juego de caracteres especificado por la propiedad **Charset**. El valor predeterminado es Unicode. La propiedad **Charset** se utiliza para convertir los datos que entran en el objeto **Stream** o que salen del objeto **Stream**. Por ejemplo, si el objeto **Stream** contiene datos ISO-8859-1 y esos datos se copian en una cadena BSTR, el objeto **Stream** convertirá los datos a Unicode, y viceversa.

En el caso de un objeto **Stream** abierto, el valor de [Position](position-property-ado.md) actual debe indicar una posición situada al comienzo del objeto **Stream** (0) para que se pueda establecer el valor de **Charset**.

**Charset** se utiliza únicamente con objetos **Stream** de texto (el valor de [Type](type-property-ado-stream.md) es **adTypeText**). Esta propiedad se omite si el valor de **Type** es **adTypeBinary**.

