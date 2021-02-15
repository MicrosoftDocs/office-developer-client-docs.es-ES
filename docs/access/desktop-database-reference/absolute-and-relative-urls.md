---
title: Direcciones URL relativas y absolutas
TOCTitle: Absolute and relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a488617dc7ba0d7d1f7e38391f8382fa1e7ed247
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282104"
---
# <a name="absolute-and-relative-urls"></a>Direcciones URL relativas y absolutas

**Se aplica a:** Access 2013, Office 2013    

Una dirección URL especifica la ubicación de un destino almacenado en un equipo local o en red, como un archivo, directorio, página HTML, imagen, programa, entre otros. En esta discusión, *una dirección URL absoluta* tiene el formato:

*esquema://servidor/ruta de acceso/recurso*

donde:

|Nombre |Descripción|
|:----|:----------|
|*esquema*|Especifica cómo se va a obtener acceso al *recurso*.|
|*servidor*|Especifica el nombre del equipo donde está ubicado el *recurso*.|
|*ruta de acceso*|Especifica la secuencia de directorios que llevan al destino. Si se omite el *recurso*, el destino es el último directorio de la *ruta de acceso*.|
|*resource*|Si se incluye, el *recurso* es el destino, que suele ser el nombre de un archivo. Puede ser un *archivo simple,* que contiene una única secuencia binaria de bytes, o un documento *estructurado,* que contiene uno o más almacenamientos y secuencias binarias de bytes.|

Una *dirección URL absoluta* contiene toda la información necesaria para localizar un recurso.

Una *dirección URL relativa* localiza un recurso mediante una dirección URL absoluta como punto de partida. En efecto, la "dirección URL completa" del destino se especifica concatenando las direcciones URL absoluta y relativa. Una dirección URL relativa normalmente se compone sólo de la *ruta de acceso* y, de manera opcional, del *recurso*, pero no del *esquema* ni del *servidor*.

## <a name="url-scheme-registration"></a>Registro del esquema de dirección URL

Si un proveedor admite direcciones URL, se registrará para uno o varios esquemas URL. Esto significa que las direcciones URL que utilicen este esquema invocarán automáticamente el proveedor registrado. Por ejemplo, el esquema *http* se registra en [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). ADO supone que todas las direcciones URL con el prefijo "http" representan carpetas web o archivos que se usarán con el proveedor de publicación en Internet. Para obtener información sobre los esquemas registrados por su proveedor, vea la documentación del proveedor.

## <a name="defining-context-with-a-url"></a>Definición de contexto con una dirección URL

Una de las funciones de una conexión abierta, representada por un objeto [Connection](connection-object-ado.md), es restringir las operaciones subsiguientes en el origen de datos representado por esa conexión. Es decir, la conexión define el contexto de las operaciones subsiguientes.

Con ADO 2.5, una dirección URL absoluta también puede definir un contexto. Por ejemplo, al abrirse un objeto [Record](record-object-ado.md) con una dirección URL absoluta, se crea implícitamente un objeto **Connection** para representar el recurso especificado por la dirección URL.

Se puede especificar una dirección URL absoluta que define un contexto en el parámetro *ActiveConnection* del método [Open](open-method-ado-record.md) del objeto **Record**. También se puede especificar una dirección URL absoluta como el valor de la palabra clave nueva en el parámetro ConnectionString del objeto Connection y el parámetro `URL=` [](open-method-ado-connection.md)  *ActiveConnection* del objeto [Recordset](recordset-object-ado.md) [Open.](open-method-ado-recordset.md) 

El contexto también se puede definir con un objeto **Record** o **Recordset** abierto que representa un directorio porque estos objetos ya tienen un objeto **Connection** implícita o explícitamente declarado que especifica el contexto.

## <a name="scoped-operations"></a>Operaciones con ámbito

El contexto define simultáneamente un *ámbito,* es decir, el directorio y sus subdirectorios que pueden participar en operaciones posteriores. El objeto **Record** tiene varios métodos con ámbito, incluidos [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md) y [DeleteRecord](deleterecord-method-ado.md), que funcionan en un directorio y todos sus subdirectorios.

## <a name="relative-urls-as-command-text"></a>Direcciones URL relativas como texto de comando

Una cadena que especifica un comando que se va a ejecutar en el origen de datos se puede especificar en el parámetro *CommandText* del método **Execute** del objeto **Connection**, y en el parámetro *Source* del método **Open** del objeto **Recordset**.

Una dirección URL relativa se puede especificar en el parámetro *CommandText* o *Source*. En realidad, la dirección URL relativa no especifica un comando (como un comando SQL); simplemente se especifica en esos parámetros. Además, el contexto de la conexión activa debe ser una dirección URL absoluta y el parámetro *Option* debe estar establecido en **adCmdTableDirect**.

Por ejemplo, un objeto **Recordset** puede abrirse en el archivo Readme25.txt del directorio Winnt/system32 de la manera siguiente:

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

La dirección URL absoluta de la cadena de conexión especifica el servidor (YourServer) y la ruta de acceso (Winnt). Esta dirección URL también define el contexto.

La dirección URL relativa del texto del comando usa la dirección URL absoluta como punto de partida y especifica el resto de la ruta de acceso (system32) y el archivo que se va a abrir (Readme25.txt).

El campo de opciones indica que el tipo de comando es una dirección URL relativa.

Como otro ejemplo, el siguiente código abrirá un **conjunto de** registros en el contenido del directorio:

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a>Esquemas de url proporcionados por el proveedor OLE DB

La parte inicial de una dirección URL completa es el *esquema* utilizado para obtener acceso al recurso identificado por el resto de la dirección URL. Por ejemplo, HTTP (Protocolo de transferencia de hipertexto) y FTP (Protocolo de transferencia de archivos).

ADO supports OLE DB providers that recognize their own URL schemes. Por ejemplo, el Proveedor de Microsoft OLE DB para publicación en [Internet,](microsoft-ole-db-provider-for-internet-publishing.md)que tiene acceso a archivos "publicados" de Windows 2000, reconoce el esquema HTTP existente.

