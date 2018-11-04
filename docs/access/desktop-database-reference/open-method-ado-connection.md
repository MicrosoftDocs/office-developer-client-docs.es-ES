---
title: Open (método, Connection de ADO)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 66a62128a8ad8828c501cdaf899448edd9f1d37f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949876"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="15787-102">Open (método, Connection de ADO)</span><span class="sxs-lookup"><span data-stu-id="15787-102">Open method (ADO Connection)</span></span>

<span data-ttu-id="15787-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15787-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="15787-104">Abre una conexión con un origen de datos.</span><span class="sxs-lookup"><span data-stu-id="15787-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="15787-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="15787-105">Syntax</span></span>

<span data-ttu-id="15787-106">*conexión*. Abra*ConnectionString*, *UserID*, *contraseña*, *Opciones*</span><span class="sxs-lookup"><span data-stu-id="15787-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="15787-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15787-107">Parameters</span></span>

|<span data-ttu-id="15787-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="15787-108">Parameter</span></span>|<span data-ttu-id="15787-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="15787-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="15787-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="15787-110">*ConnectionString*</span></span> |<span data-ttu-id="15787-p101">Es opcional. Valor de tipo **String** que contiene la información de conexión. Vea la propiedad [ConnectionString](connectionstring-property-ado.md) para obtener información detallada sobre los valores de configuración válidos.</span><span class="sxs-lookup"><span data-stu-id="15787-p101">Optional. A **String** value that contains connection information. See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>|
|<span data-ttu-id="15787-114">*UserID*</span><span class="sxs-lookup"><span data-stu-id="15787-114">*UserID*</span></span> |<span data-ttu-id="15787-p102">Es opcional. Valor de tipo **String** que contiene el nombre de usuario que se va a utilizar para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="15787-p102">Optional. A **String** value that contains a user name to use when establishing the connection.</span></span>|
|<span data-ttu-id="15787-117">*Password*</span><span class="sxs-lookup"><span data-stu-id="15787-117">*Password*</span></span> |<span data-ttu-id="15787-p103">Es opcional. Valor de tipo **String** que contiene la contraseña que se va a utilizar para establecer la conexión.</span><span class="sxs-lookup"><span data-stu-id="15787-p103">Optional. A **String** value that contains a password to use when establishing the connection.</span></span>|
|<span data-ttu-id="15787-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="15787-120">*Options*</span></span> |<span data-ttu-id="15787-p104">Es opcional. Valor de [ConnectOptionEnum](connectoptionenum.md) que determina si este método debe devolver un valor después (sincrónicamente) o antes (asincrónicamentep>) de que se establezca la conexión.</span><span class="sxs-lookup"><span data-stu-id="15787-p104">Optional. A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>|

## <a name="remarks"></a><span data-ttu-id="15787-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="15787-123">Remarks</span></span>

<span data-ttu-id="15787-p105">Si se utiliza el método **Open** en un objeto [Connection](connection-object-ado.md), se establece la conexión física con un origen de datos. Tras finalizar correctamente este método, la conexión está activa y se pueden emitir comandos y procesar los resultados.</span><span class="sxs-lookup"><span data-stu-id="15787-p105">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source. After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="15787-126">Use el argumento opcional *ConnectionString* para especificar una cadena de conexión que contiene una serie de instrucciones de *argumento* *= valor* separadas por punto y coma, o un archivo o recurso de Active directory identificado con una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="15787-126">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="15787-127">La propiedad **ConnectionString** hereda automáticamente el valor utilizado para el argumento *ConnectionString* .</span><span class="sxs-lookup"><span data-stu-id="15787-127">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="15787-128">Por lo tanto, puede establecer la propiedad **ConnectionString** del objeto **Connection** antes de abrirlo, o use el argumento *ConnectionString* para establecer o reemplazar los actuales parámetros de conexión durante la llamada al método **Open** .</span><span class="sxs-lookup"><span data-stu-id="15787-128">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="15787-129">Si pasa la información de usuario y de contraseña en el argumento *ConnectionString* y en los argumentos opcionales *UserID* y *Password*, los argumentos *UserID* y *Password* invalidarán los valores especificados en *ConnectionString*.</span><span class="sxs-lookup"><span data-stu-id="15787-129">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="15787-p107">Una vez finalizadas las operaciones en un objeto **Connection** abierto, use el método [Close](close-method-ado.md) para liberar los recursos del sistema asociados. Cerrar un objeto no lo quita de la memoria; puede cambiar los valores de sus propiedades y volver a abrirlo más adelante mediante el método **Open**. Para eliminar completamente un objeto de la memoria, establezca el valor de la variable del objeto en *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="15787-p107">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources. Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later. To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="15787-133">**Uso de servicio de datos remotos** Cuando se usa en un objeto **Connection** de cliente, el método **Open** no establece una conexión con el servidor hasta que se abre un [objeto Recordset](recordset-object-ado.md) en el objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="15787-133">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="15787-134">[!NOTA] Las direcciones URL que utilicen el esquema http invocarán automáticamente [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="15787-134">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="15787-135">Para obtener más información, vea [direcciones URL absolutas y relativas](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="15787-135">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


