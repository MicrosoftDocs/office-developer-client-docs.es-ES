---
title: Open (método, Record de ADO)
TOCTitle: Open method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: db8953cafc5ad266c81c51e59cbf92787d07cdfb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288381"
---
# <a name="open-method-ado-record"></a>Open (método, Record de ADO)

**Se aplica a:** Access 2013, Office 2013

Abre un objeto [Record](record-object-ado.md) existente o crea un nuevo elemento representado por el objeto **Record** (como un archivo o un directorio).

## <a name="syntax"></a>Sintaxis

Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*

## <a name="parameters"></a>Parámetros

|Parámetro|Descripción|
|:--------|:----------|
|*Source* |Es opcional. **Variant** que puede representar la dirección URL de la entidad que va a representar este objeto **Record**, un objeto **Command**, un objeto [Recordset](recordset-object-ado.md) abierto u otro objeto **Record**, una cadena que contiene una instrucción SQL SELECT o un nombre de tabla.|
|*ActiveConnection* | Es opcional. **Variant** que representa la cadena de conexión o el objeto [Connection](connection-object-ado.md) abierto.|
|*Mode* |Es opcional. Valor de [ConnectModeEnum](connectmodeenum.md), cuyo valor predeterminado es **adModeUnknown**, que especifica el modo de acceso del objeto **Record** resultante.|
|*CreateOptions* |Es opcional. Valor de [RecordCreateOptionsEnum](recordcreateoptionsenum.md), cuyo valor predeterminado es **adFailIfNotExists**, que especifica si debe haber un archivo o directorio abierto o si debe crearse un nuevo archivo o directorio. Si está especificado el valor predeterminado, el modo de acceso se obtiene de la propiedad [Mode](mode-property-ado.md). Este parámetro se omite cuando el parámetro *Source* no contiene una dirección URL.|
|*Options* |Es opcional. Valor de [RecordOpenOptionsEnum](recordopenoptionsenum.md), cuyo valor predeterminado es **adOpenRecordUnspecified**, que especifica las opciones para abrir el objeto **Record**. Estos valores se pueden combinar.|
|*UserName* |Es opcional. Valor de tipo **String** con el identificador de usuario que, en caso de que sea necesario, autoriza el acceso a *Source*.|
|*Password* |Opcional. Valor de tipo **String** con la contraseña que, en caso de que sea necesario, comprueba *UserName*.|

## <a name="remarks"></a>Comentarios

*Source* puede ser:

- Una dirección URL. Si el protocolo de la dirección URL es http, se invocará de forma predeterminada el proveedor de Internet. Si la dirección URL señala un nodo que contiene un script ejecutable (como una página .ASP), se abre de manera predeterminada un objeto **Record** que contiene el origen en lugar del contenido ejecutado. Use el argumento *Options* para modificar este comportamiento.

- Un objeto **Record**. Un objeto **Record** que se abre desde otro objeto **Record** duplicará el objeto **Record** original.

- Un objeto **Command**. El objeto **Record** abierto representa la fila devuelta por la ejecución del objeto **Command**. Si los resultados contienen más de una fila, el contenido de la primera fila se ubica en el registro y puede que se agregue un error a la colección **Errors**.

- Una instrucción SQL SELECT. El objeto **Record** abierto representa la fila devuelta por la ejecución del contenido de la cadena. Si los resultados contienen más de una fila, el contenido de la primera fila se ubica en el registro y puede que se agregue un error a la colección **Errors**.

- Un nombre de tabla.

Si el objeto **Record** representa una entidad a la que no se puede obtener acceso con una dirección URL (por ejemplo, una fila de un objeto **Recordset** derivado de una base de datos), los valores de la propiedad [ParentURL](parenturl-property-ado.md) y del campo al que se obtiene acceso con la constante **adRecordURL** son null.

> [!NOTE]
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [Direcciones URL absolutas y relativas.](absolute-and-relative-urls.md)


