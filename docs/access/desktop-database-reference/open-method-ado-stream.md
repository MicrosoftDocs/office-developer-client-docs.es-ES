---
title: Open (método, Stream de ADO)
TOCTitle: Open method (ADO Stream)
ms:assetid: fa2e6aaa-e9f5-009c-f3a0-050a00abf9b0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250275(v=office.15)
ms:contentKeyID: 48548833
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a943209ce329d59fb4846ed18fd008bc45803da
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715546"
---
# <a name="open-method-ado-stream"></a>Open (método, Stream de ADO)


**Se aplica a**: Access 2013, Office 2013


Abre un objeto [Stream](stream-object-ado.md) para manipular secuencias de datos binarios o de texto.

## <a name="syntax"></a>Sintaxis

*Secuencia*. Abrir *origen*, *modo*, *adOpenStreamFromRecord*, *nombre de usuario*, *contraseña*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Source* |Es opcional. Valor de tipo **Variant** que especifica el origen de datos del objeto **Stream**. *Source* puede contener una cadena de dirección URL absoluta que apunta a un nodo existente en una estructura de árbol conocida, como un sistema de correo electrónico o un archivo. Una dirección URL debe especificarse mediante la palabra clave URL ("URL =*combinación*://*server*/*carpeta*"). Asimismo, *Source* puede contener una referencia a un objeto [Record](record-object-ado.md) ya está abierto, que abre la secuencia predeterminada asociada con el **registro**. Si no se especifica *Source* , una **secuencia** se crea una instancia y se abre, asociada a ningún origen subyacente de forma predeterminada. Para obtener más información sobre los esquemas URL y sus proveedores asociados, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).|
|*Mode* |Es opcional. Valor de [ConnectModeEnum](connectmodeenum.md) que especifica el modo de acceso del objeto **Stream** resultante (por ejemplo, de lectura y escritura, o bien, de solo lectura). El valor predeterminado es **adModeUnknown**. Vea la propiedad [Mode](mode-property-ado.md) para obtener más información sobre los modos de acceso. Si no se especifica el *modo* , es heredada por el objeto de origen. Por ejemplo, si el objeto **Record** de origen se abre en modo de solo lectura, el objeto **Stream** también se abrirá de forma predeterminada en modo de solo lectura.|
|*AdOpenStreamFromRecord* |Es opcional. Valor de [StreamOpenOptionsEnum](streamopenoptionsenum.md). El valor predeterminado es **adOpenStreamUnspecified**.|
|*UserName* |Es opcional. Valor de tipo **String** con la identificación del usuario que, en caso de que sea necesario, obtiene acceso al objeto **Stream**.|
|*Password* |Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, obtiene acceso al objeto **Stream**.|

## <a name="remarks"></a>Comentarios

No se usan cuando un objeto **Record** se pasa como el parámetro source, el *identificador de usuario* y los parámetros de *contraseña* debido a que el acceso al objeto **Record** ya está disponible. De forma similar, el [modo](mode-property-ado.md) del objeto **Record** se transfiere al objeto **Stream** . Cuando no se especifica el *origen* , la **secuencia** abierta no contiene datos y tiene un [tamaño](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de cero (0). Para evitar la pérdida de los datos que se escriben en esta **secuencia** cuando está cerrada la **secuencia** , guardar la **secuencia** con los métodos [CopyTo](copyto-method-ado.md) o [SaveToFile](savetofile-method-ado.md) , o a otra ubicación de memoria.

Un valor *adOpenStreamFromRecord* de **OpenOptions** identifica el contenido del parámetro *Source* como un objeto **Record** ya está abierto. El comportamiento predeterminado es tratar *Source* como una dirección URL que señala directamente a un nodo en una estructura de árbol, como un archivo. Se abre la secuencia predeterminada asociada a ese nodo.

Mientras no esté abierto el objeto **Stream**, es posible leer todas las propiedades de solo lectura de **Stream**. Si se abre un objeto **Stream** asincrónicamente, todas las operaciones subsiguientes (que no sean la comprobación de [State](state-property-ado.md) y otras propiedades de solo lectura) se bloquean hasta que finalice la operación **Open**.

Además de las opciones anteriormente descritas, si no se especifica el valor de *Source*, se puede crear simplemente una instancia de un objeto **Stream** en la memoria sin asociarla a un origen subyacente. Se pueden agregar datos dinámicamente a la secuencia escribiendo simplemente datos binarios o de texto en el objeto **Stream** mediante [Write](write-method-ado.md) o [WriteText](writetext-method-ado.md), o bien, cargando los datos desde un archivo mediante [LoadFromFile](loadfromfile-method-ado.md).

