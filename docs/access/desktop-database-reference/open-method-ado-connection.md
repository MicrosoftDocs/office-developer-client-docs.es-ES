---
title: Open (método, Objeto Connection de ADO)
TOCTitle: Open Method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3bd698f7ea6c05d81e07969ae8031049804b7706
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889472"
---
# <a name="open-method-ado-connection"></a>Open (método, Objeto Connection de ADO)


**Se aplica a**: Access 2013, Office 2013
 

Abre una conexión con un origen de datos.

## <a name="syntax"></a>Sintaxis

*conexión*. Abra*ConnectionString*, *UserID*, *contraseña*, *Opciones*

## <a name="parameters"></a>Parámetros

  - *ConnectionString*

  - Es opcional. Valor de tipo **String** que contiene la información de conexión. Vea la propiedad [ConnectionString](connectionstring-property-ado.md) para obtener información detallada sobre los valores de configuración válidos.

  - *UserID*

  - Es opcional. Valor de tipo **String** que contiene el nombre de usuario que se va a utilizar para establecer la conexión.

  - *Password*

  - Es opcional. Valor de tipo **String** que contiene la contraseña que se va a utilizar para establecer la conexión.

  - *Options*

  - Es opcional. Valor de [ConnectOptionEnum](connectoptionenum.md) que determina si este método debe devolver un valor después (sincrónicamente) o antes (asincrónicamentep>) de que se establezca la conexión.

## <a name="remarks"></a>Comentarios

Si se utiliza el método **Open** en un objeto [Connection](connection-object-ado.md), se establece la conexión física con un origen de datos. Tras finalizar correctamente este método, la conexión está activa y se pueden emitir comandos y procesar los resultados.

Use el argumento opcional *ConnectionString* para especificar una cadena de conexión que contiene una serie de instrucciones de *argumento* *= valor* separadas por punto y coma, o un archivo o recurso de Active directory identificado con una dirección URL. La propiedad **ConnectionString** hereda automáticamente el valor utilizado para el argumento *ConnectionString* . Por lo tanto, puede establecer la propiedad **ConnectionString** del objeto **Connection** antes de abrirlo, o use el argumento *ConnectionString* para establecer o reemplazar los actuales parámetros de conexión durante la llamada al método **Open** .

Si pasa la información de usuario y de contraseña en el argumento *ConnectionString* y en los argumentos opcionales *UserID* y *Password*, los argumentos *UserID* y *Password* invalidarán los valores especificados en *ConnectionString*.

Una vez finalizadas las operaciones en un objeto **Connection** abierto, use el método [Close](close-method-ado.md) para liberar los recursos del sistema asociados. Cerrar un objeto no lo quita de la memoria; puede cambiar los valores de sus propiedades y volver a abrirlo más adelante mediante el método **Open**. Para eliminar completamente un objeto de la memoria, establezca el valor de la variable del objeto en *Nothing*.

**Uso de servicio de datos remotos** Cuando se usa en un objeto **Connection** de cliente, el método **Open** no establece una conexión con el servidor hasta que se abre un [objeto Recordset](recordset-object-ado.md) en el objeto **Connection** .


> [!NOTE]
> [!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).


