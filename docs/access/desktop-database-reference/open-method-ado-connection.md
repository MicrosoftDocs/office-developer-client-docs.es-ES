---
title: Open (método, Connection de ADO)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288430"
---
# <a name="open-method-ado-connection"></a>Open (método, Connection de ADO)

**Se aplica a:** Access 2013, Office 2013
 
Abre una conexión con un origen de datos.

## <a name="syntax"></a>Sintaxis

*conexión*. Abrir*ConnectionString*, *userid*, *password*, *Options*

## <a name="parameters"></a>Parámetros

|Parameter|Descripción|
|:--------|:----------|
|*ConnectionString* |Es opcional. Valor de tipo **String** que contiene la información de conexión. Vea la propiedad [ConnectionString](connectionstring-property-ado.md) para obtener información detallada sobre los valores de configuración válidos.|
|*UserID* |Es opcional. Valor de tipo **String** que contiene el nombre de usuario que se va a utilizar para establecer la conexión.|
|*Password* |Es opcional. Valor de tipo **String** que contiene la contraseña que se va a utilizar para establecer la conexión.|
|*Options* |Es opcional. Valor de [ConnectOptionEnum](connectoptionenum.md) que determina si este método debe devolver un valor después (sincrónicamente) o antes (asincrónicamentep>) de que se establezca la conexión.|

## <a name="remarks"></a>Comentarios

Si se utiliza el método **Open** en un objeto [Connection](connection-object-ado.md), se establece la conexión física con un origen de datos. Tras finalizar correctamente este método, la conexión está activa y se pueden emitir comandos y procesar los resultados.

Utilice el argumento opcional *ConnectionString* para especificar una cadena de conexión que contenga una serie de instrucciones *argument* *= Value* separadas por punto y coma, o un recurso de archivo o directorio identificado con una dirección URL. La propiedad **ConnectionString** hereda automáticamente el valor usado para el argumento *ConnectionString*. Por ello, puede establecer la propiedad **ConnectionString** del objeto **Connection** antes de abrirlo, o bien, usar el argumento *ConnectionString* para establecer o invalidar los actuales parámetros de conexión durante la llamada al método **Open**.

Si pasa la información de usuario y de contraseña en el argumento *ConnectionString* y en los argumentos opcionales *UserID* y *Password*, los argumentos *UserID* y *Password* invalidarán los valores especificados en *ConnectionString*.

Una vez finalizadas las operaciones en un objeto **Connection** abierto, use el método [Close](close-method-ado.md) para liberar los recursos del sistema asociados. Cerrar un objeto no lo quita de la memoria; puede cambiar los valores de sus propiedades y volver a abrirlo más adelante mediante el método **Open**. Para eliminar completamente un objeto de la memoria, establezca el valor de la variable del objeto en *Nothing*.

**Uso del servicio de datos remotos** Cuando se usa en un objeto **Connection** del cliente, el método **Open** no establece una conexión con el servidor hasta que se abra un objeto [Recordset](recordset-object-ado.md) en el objeto **Connection** .

> [!NOTE]
> [!NOTA] Las direcciones URL que utilizan el esquema http llamarán automáticamente a [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).


