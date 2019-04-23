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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288388"
---
# <a name="open-method-ado-stream"></a>Open (método, Stream de ADO)


**Se aplica a:** Access 2013, Office 2013


Abre un objeto [Stream](stream-object-ado.md) para manipular secuencias de datos binarios o de texto.

## <a name="syntax"></a>Sintaxis

*Secuencia*. Abrir *origen*, *modo*, *el*, *nombre de usuario*, *contraseña*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*Source* |Es opcional. Valor de tipo **Variant** que especifica el origen de datos del objeto **Stream**. *Source* puede contener una cadena URL absoluta que apunta a un nodo existente en una estructura de árbol conocida, como un correo electrónico o un sistema de archivos. Una dirección URL debe especificarse mediante la palabra clave URL ("URL =*Scheme*://*carpeta*del*servidor*/"). Asimismo, *Source* puede contener una referencia a un objeto [Record](record-object-ado.md) abierto, que abre la secuencia predeterminada asociada al objeto **Record**. Si no se especifica *Source*, se crea y se abre una instancia de **Stream**, que no está asociada a ningún origen subyacente de manera predeterminada. Para obtener más información acerca de los esquemas de direcciones URL y sus proveedores asociados, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).|
|*Mode* |Es opcional. Valor de [ConnectModeEnum](connectmodeenum.md) que especifica el modo de acceso del objeto **Stream** resultante (por ejemplo, de lectura y escritura, o bien, de solo lectura). El valor predeterminado es **adModeUnknown**. Vea la propiedad [Mode](mode-property-ado.md) para obtener más información sobre los modos de acceso. Si no se especifica *Mode*, su valor se hereda del objeto de origen. Por ejemplo, si el objeto **Record** de origen se abre en modo de solo lectura, el objeto **Stream** también se abrirá de forma predeterminada en modo de solo lectura.|
|*El* |Es opcional. Valor de [StreamOpenOptionsEnum](streamopenoptionsenum.md). El valor predeterminado es **adOpenStreamUnspecified**.|
|*UserName* |Es opcional. Valor de tipo **String** con la identificación del usuario que, en caso de que sea necesario, obtiene acceso al objeto **Stream**.|
|*Password* |Es opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, obtiene acceso al objeto **Stream**.|

## <a name="remarks"></a>Comentarios

Cuando se pasa un objeto **Record** como parámetro de origen, no se utilizan los parámetros *UserID* y *Password* porque el acceso al objeto **Record** ya está disponible. De manera similar, el valor de [Mode](mode-property-ado.md) del objeto **Record** se transfiere al objeto **Stream**. Cuando no se especifica el valor de *Source*, el objeto **Stream** abierto no contiene datos y su valor de [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) es cero (0). Para evitar que se pierdan los datos escritos en este objeto **Stream** cuando se cierra el objeto **Stream**, guarde el objeto **Stream** con el método [CopyTo](copyto-method-ado.md) o [SaveToFile](savetofile-method-ado.md), o bien, guárdelo en otra ubicación de la memoria.

El valor **adOpenStreamFromRecord** de *OpenOptions* identifica el contenido del parámetro *Source* como un objeto **Record** abierto. El comportamiento predeterminado es tratar *Source* como una dirección URL que señala directamente un nodo en una estructura de árbol, como un archivo. Se abre la secuencia predeterminada asociada a ese nodo.

Mientras no esté abierto el objeto **Stream**, es posible leer todas las propiedades de solo lectura de **Stream**. Si se abre un objeto **Stream** asincrónicamente, todas las operaciones subsiguientes (que no sean la comprobación de [State](state-property-ado.md) y otras propiedades de solo lectura) se bloquean hasta que finalice la operación **Open**.

Además de las opciones anteriormente descritas, si no se especifica el valor de *Source*, se puede crear simplemente una instancia de un objeto **Stream** en la memoria sin asociarla a un origen subyacente. Se pueden agregar datos dinámicamente a la secuencia escribiendo simplemente datos binarios o de texto en el objeto **Stream** mediante [Write](write-method-ado.md) o [WriteText](writetext-method-ado.md), o bien, cargando los datos desde un archivo mediante [LoadFromFile](loadfromfile-method-ado.md).

