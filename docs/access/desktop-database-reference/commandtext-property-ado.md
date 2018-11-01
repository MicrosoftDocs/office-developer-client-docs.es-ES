---
title: CommandText (propiedad, ADO)
TOCTitle: CommandText property (ADO)
ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15)
ms:contentKeyID: 48543234
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231123
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 86f69be8ed9216619f10bc70e2c701fb109d0ff5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879308"
---
# <a name="commandtext-property-ado"></a>CommandText (propiedad, ADO)


**Se aplica a**: Access 2013, Office 2013

Indica el texto de un comando que se va a emitir en un proveedor.

## <a name="settings-and-return-values"></a>Configuración y valores devueltos

Establece o devuelve un valor de tipo **String** que contiene un comando de proveedor, como una instrucción SQL, un nombre de tabla, una dirección URL relativa o una llamada a un procedimiento almacenado. El valor predeterminado es "" (cadena de longitud cero).

## <a name="remarks"></a>Comentarios

Utilice la propiedad **CommandText** para establecer o devolver el texto de un comando representado por un objeto [Command](command-object-ado.md). Normalmente es una instrucción SQL, pero también puede ser cualquier otro tipo de instrucción de comando que reconozca el proveedor, como una llamada a un procedimiento almacenado. El procesador de consultas del proveedor debe admitir el dialecto o la versión de la instrucción SQL.

Si la propiedad [Prepared](prepared-property-ado.md) del objeto **Command** tiene el valor **True** y el objeto **Command** está enlazado a una conexión abierta cuando se establece el valor de la propiedad **CommandText**, ADO preparará la consulta (es decir, una forma compilada de la consulta que el proveedor almacena) cuando se llame a los métodos [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) u **Open**.

Dependiendo del valor de la propiedad [CommandType](commandtype-property-ado.md), puede que ADO modifique la propiedad **CommandText**. La propiedad **CommandText** se puede leer en cualquier momento para ver el texto real del comando que ADO va a utilizar durante la ejecución.

Utilice la propiedad **CommandText** para establecer o devolver una dirección URL relativa que especifica un recurso, como un archivo o un directorio. El recurso es relativo a una ubicación especificada explícitamente por una dirección URL absoluta o implícitamente por un objeto [Connection](connection-object-ado.md) abierto.


> [!NOTE]
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).


