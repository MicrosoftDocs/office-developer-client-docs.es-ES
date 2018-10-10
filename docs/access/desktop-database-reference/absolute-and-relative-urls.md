---
title: Direcciones URL absolutas y relativas
TOCTitle: Absolute and Relative URLs
ms:assetid: 79a1f793-7154-1c13-7dfe-a1b8cd64e1ea
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249501(v=office.15)
ms:contentKeyID: 48545774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6bc0cb3086f8fdfa032c005f7e2d219dab56999b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25486089"
---
# <a name="absolute-and-relative-urls"></a><span data-ttu-id="8da44-102">Direcciones URL absolutas y relativas</span><span class="sxs-lookup"><span data-stu-id="8da44-102">Absolute and Relative URLs</span></span>

<span data-ttu-id="8da44-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8da44-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="8da44-p101">Una dirección URL especifica la ubicación de un destino almacenado en un equipo local o conectado en red, como un archivo, un directorio, una página HTML, una imagen, un programa, etc.\*\* En este tema, una *dirección URL absoluta* tiene el siguiente formato:</span><span class="sxs-lookup"><span data-stu-id="8da44-p101">A URL specifies the location of a target stored on a local or networked computer, such as a file, directory, HTML page, image, program, and so on *.* In this discussion, an *absolute URL* is of the form:</span></span>

<span data-ttu-id="8da44-106">*esquema://servidor/ruta de acceso/recurso*</span><span class="sxs-lookup"><span data-stu-id="8da44-106">*scheme://server/path/resource*</span></span>

<span data-ttu-id="8da44-107">donde:</span><span class="sxs-lookup"><span data-stu-id="8da44-107">where:</span></span>

  - <span data-ttu-id="8da44-108">*esquema*</span><span class="sxs-lookup"><span data-stu-id="8da44-108">*scheme*</span></span>

  - <span data-ttu-id="8da44-109">Especifica cómo se puede tener acceso a los *recursos* .</span><span class="sxs-lookup"><span data-stu-id="8da44-109">Specifies how the *resource* is to be accessed.</span></span>

  - <span data-ttu-id="8da44-110">*servidor*</span><span class="sxs-lookup"><span data-stu-id="8da44-110">*server*</span></span>

  - <span data-ttu-id="8da44-111">Especifica el nombre del equipo donde está ubicado el *recurso* .</span><span class="sxs-lookup"><span data-stu-id="8da44-111">Specifies the name of the computer where the *resource* is located.</span></span>

  - <span data-ttu-id="8da44-112">*ruta de acceso*</span><span class="sxs-lookup"><span data-stu-id="8da44-112">*path*</span></span>

  - <span data-ttu-id="8da44-p102">Especifica la secuencia de directorios que llevan al destino. Si se omite el *recurso*, el destino es el último directorio de la *ruta de acceso*.</span><span class="sxs-lookup"><span data-stu-id="8da44-p102">Specifies the sequence of directories leading to the target. If *resource* is omitted, the target is the last directory in *path*.</span></span>

  - <span data-ttu-id="8da44-115">*recurso*</span><span class="sxs-lookup"><span data-stu-id="8da44-115">*resource*</span></span>

  - <span data-ttu-id="8da44-116">Si se incluye, *recurso* es el destino y normalmente es el nombre de un archivo.</span><span class="sxs-lookup"><span data-stu-id="8da44-116">If included, *resource* is the target, and is typically the name of a file.</span></span> <span data-ttu-id="8da44-117">Puede ser un *archivo simple,* que contiene una única secuencia binaria de bytes o un *documento estructurado,* que contiene uno o varios almacenamientos y secuencias binarias de bytes.</span><span class="sxs-lookup"><span data-stu-id="8da44-117">It may be a *simple file,* containing a single binary stream of bytes, or a *structured document,* containing one or more storages and binary streams of bytes.</span></span>

<span data-ttu-id="8da44-118">Una *dirección URL absoluta* contiene toda la información necesaria para localizar un recurso.</span><span class="sxs-lookup"><span data-stu-id="8da44-118">An *absolute URL* contains all the information necessary to locate a resource.</span></span>

<span data-ttu-id="8da44-p104">Una *dirección URL relativa* localiza un recurso mediante una dirección URL absoluta como punto de partida. En efecto, la "dirección URL completa" del destino se especifica concatenando las direcciones URL absoluta y relativa. Una dirección URL relativa normalmente se compone sólo de la *ruta de acceso* y, de manera opcional, del *recurso*, pero no del *esquema* ni del *servidor*.</span><span class="sxs-lookup"><span data-stu-id="8da44-p104">A *relative URL* locates a resource using an absolute URL as a starting point. In effect, the "complete URL" of the target is specified by concatenating the absolute and relative URLs. A relative URL typically consists only of the *path*, and optionally, the *resource*, but no *scheme* or *server*.</span></span>

## <a name="url-scheme-registration"></a><span data-ttu-id="8da44-122">Registro de esquemas URL</span><span class="sxs-lookup"><span data-stu-id="8da44-122">URL Scheme Registration</span></span>

<span data-ttu-id="8da44-123">Si un proveedor admite direcciones URL, se registrará para uno o varios esquemas URL.</span><span class="sxs-lookup"><span data-stu-id="8da44-123">If a provider supports URLs, it will register for one or more URL schemes.</span></span> <span data-ttu-id="8da44-124">Esto significa que las direcciones URL que utilicen este esquema invocarán automáticamente el proveedor registrado.</span><span class="sxs-lookup"><span data-stu-id="8da44-124">This means that any URLs using this scheme will automatically invoke the registered provider.</span></span> <span data-ttu-id="8da44-125">Por ejemplo, el esquema *http* se registra para el [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="8da44-125">For example, the *http* scheme is registered to the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="8da44-126">ADO da por supuesto que todas las direcciones URL precedidas del prefijo "http" representan carpetas o archivos Web que deben utilizarse con el proveedor de publicaciones en Internet.</span><span class="sxs-lookup"><span data-stu-id="8da44-126">ADO assumes all URLs prefixed with "http" represent Web folders or files to be used with the Internet Publishing Provider.</span></span> <span data-ttu-id="8da44-127">Para obtener información sobre los esquemas registrados por su proveedor, vea la documentación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="8da44-127">For information about the schemes registered by your provider, see your provider documentation.</span></span>

## <a name="defining-context-with-a-url"></a><span data-ttu-id="8da44-128">Definir contexto con una dirección URL</span><span class="sxs-lookup"><span data-stu-id="8da44-128">Defining Context with a URL</span></span>

<span data-ttu-id="8da44-p106">Una de las funciones de una conexión abierta, representada por un objeto [Connection](connection-object-ado.md), es restringir las operaciones subsiguientes en el origen de datos representado por esa conexión. Es decir, la conexión define el contexto de las operaciones subsiguientes.</span><span class="sxs-lookup"><span data-stu-id="8da44-p106">One function of an open connection, represented by a [Connection](connection-object-ado.md) object, is to restrict subsequent operations to the data source represented by that connection. That is, the connection defines the context for subsequent operations.</span></span>

<span data-ttu-id="8da44-p107">Con ADO 2.5, una dirección URL absoluta también puede definir un contexto. Por ejemplo, al abrirse un objeto [Record](record-object-ado.md) con una dirección URL absoluta, se crea implícitamente un objeto **Connection** para representar el recurso especificado por la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8da44-p107">With ADO 2.5, an absolute URL may also define a context. For example, when a [Record](record-object-ado.md) object is opened with an absolute URL, a **Connection** object is implicitly created to represent the resource specified by the URL.</span></span>

<span data-ttu-id="8da44-133">Una dirección URL absoluta que define un contexto puede especificarse en el parámetro *ActiveConnection* del método [Open](open-method-ado-record.md) del objeto de **registro** .</span><span class="sxs-lookup"><span data-stu-id="8da44-133">An absolute URL that defines a context may be specified in the *ActiveConnection* parameter of the **Record** object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="8da44-134">También se puede especificar una dirección URL absoluta como el valor de la nueva "dirección URL**=**" palabra clave en la **conexión de** objeto [Open](open-method-ado-connection.md) parámetro *ConnectionString* del método y el objeto [Recordset](recordset-object-ado.md) \*ActiveConnection del método [Open](open-method-ado-recordset.md) \*parámetro.</span><span class="sxs-lookup"><span data-stu-id="8da44-134">An absolute URL may also be specified as the value of the new "URL**=**" keyword in the **Connection** object [Open](open-method-ado-connection.md) method *ConnectionString* parameter, and the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method *ActiveConnection* parameter.</span></span>

<span data-ttu-id="8da44-135">El contexto también se puede definir con un objeto **Record** o **Recordset** abierto que representa un directorio porque estos objetos ya tienen un objeto **Connection** implícita o explícitamente declarado que especifica el contexto.</span><span class="sxs-lookup"><span data-stu-id="8da44-135">Context may also be defined with an open **Record** or **Recordset** object that represents a directory because these objects already have an implicitly or explicitly declared **Connection** object that specifies context.</span></span>

## <a name="scoped-operations"></a><span data-ttu-id="8da44-136">Operaciones con ámbito</span><span class="sxs-lookup"><span data-stu-id="8da44-136">Scoped Operations</span></span>

<span data-ttu-id="8da44-137">El contexto define a la vez un *ámbito* ; es decir, el directorio y sus subdirectorios que pueden participar en las siguientes operaciones.</span><span class="sxs-lookup"><span data-stu-id="8da44-137">The context simultaneously defines a *scope* — that is, the directory and its subdirectories that may participate in subsequent operations.</span></span> <span data-ttu-id="8da44-138">El objeto **Record** tiene varios métodos con ámbito, incluidos [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md) y [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), que funcionan en un directorio y todos sus subdirectorios.</span><span class="sxs-lookup"><span data-stu-id="8da44-138">The **Record** object has several scoped methods, including [CopyRecord](copyrecord-method-ado.md), [MoveRecord](moverecord-method-ado.md), and [DeleteRecord](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), that operate on a directory and all its subdirectories.</span></span>

## <a name="relative-urls-as-command-text"></a><span data-ttu-id="8da44-139">Direcciones URL relativas como texto de comando</span><span class="sxs-lookup"><span data-stu-id="8da44-139">Relative URLs as Command Text</span></span>

<span data-ttu-id="8da44-140">Una cadena que especifica un comando que se ejecutará en el origen de datos puede especificarse en el parámetro *CommandText* del método de **conexión** objeto **Execute** y el parámetro del *origen de* **conjunto de registros de** objeto **Open** (método).</span><span class="sxs-lookup"><span data-stu-id="8da44-140">A string specifying a command to be executed on the data source may be specified in the **Connection** object **Execute** method *CommandText* parameter, and the **Recordset** object **Open** method *Source* parameter.</span></span>

<span data-ttu-id="8da44-141">Una dirección URL relativa se puede especificar en el parámetro *CommandText* o *Source* .</span><span class="sxs-lookup"><span data-stu-id="8da44-141">A relative URL may be specified in the *CommandText* or *Source* parameter.</span></span> <span data-ttu-id="8da44-142">En realidad, la dirección URL relativa no especifica un comando (como un comando SQL); simplemente se especifica en esos parámetros.</span><span class="sxs-lookup"><span data-stu-id="8da44-142">The relative URL does not actually specify a command (such as an SQL command); it is merely specified in those parameters.</span></span> <span data-ttu-id="8da44-143">Además, el contexto de la conexión activa debe ser una dirección URL absoluta y el parámetro *opción* debe establecerse en **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="8da44-143">In addition, the context of the active connection must be an absolute URL, and the *Option* parameter must be set to **adCmdTableDirect**.</span></span>

<span data-ttu-id="8da44-144">Por ejemplo, un objeto **Recordset** puede abrirse en el archivo Readme25.txt del directorio Winnt/system32 de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="8da44-144">For example, a **Recordset** could be opened on the Readme25.txt file of the Winnt/system32 directory like this:</span></span>

```vb
recordset.Open "system32/Readme25.txt", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

<span data-ttu-id="8da44-145">La dirección URL absoluta en la cadena de conexión especifica el servidor (YourServer) y el () de la ruta de acceso y la ruta de acceso (Winnt).</span><span class="sxs-lookup"><span data-stu-id="8da44-145">The absolute URL in the connection string specifies the server (YourServer ) and the path () and the path (Winnt ).</span></span> <span data-ttu-id="8da44-146">Esta dirección URL también define el contexto.</span><span class="sxs-lookup"><span data-stu-id="8da44-146">This URL also defines the context.</span></span>

<span data-ttu-id="8da44-147">La dirección URL relativa en el texto de comando utiliza la dirección URL absoluta como punto de partida y especifica el resto de la ruta de acceso (system32) y el archivo para abrir () y el archivo para abrir (Readme25.txt).</span><span class="sxs-lookup"><span data-stu-id="8da44-147">The relative URL in the command text uses the absolute URL as a starting point and specifies the remainder of the path (system32 ) and the file to open () and the file to open (Readme25.txt ).</span></span>

<span data-ttu-id="8da44-148">El campo de opciones () indica que el tipo de comando es una dirección URL relativa.</span><span class="sxs-lookup"><span data-stu-id="8da44-148">The options field () indicates that the command type is a relative URL.</span></span>

<span data-ttu-id="8da44-149">Como otro ejemplo, el siguiente código abrirá un **objeto Recordset** en el contenido del directorio:</span><span class="sxs-lookup"><span data-stu-id="8da44-149">As another example, the following code will open a **Recordset** on the contents of the directory:</span></span>

```vb
recordset.Open "", "URL=https://YourServer/Winnt/",,,adCmdTableDirect 
```

## <a name="ole-db-provider-supplied-url-schemes"></a><span data-ttu-id="8da44-150">Esquemas de direcciones URL proporcionados por el proveedor OLE DB</span><span class="sxs-lookup"><span data-stu-id="8da44-150">OLE DB Provider-Supplied URL Schemes</span></span>

<span data-ttu-id="8da44-151">La parte inicial de una dirección URL completa es el *esquema* utilizado para obtener acceso al recurso identificado por el resto de la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="8da44-151">The leading part of a fully-qualified URL is the *scheme* used to access the resource identified by the remainder of the URL.</span></span> <span data-ttu-id="8da44-152">Por ejemplo, HTTP (Protocolo de transferencia de hipertexto) y FTP (Protocolo de transferencia de archivos).</span><span class="sxs-lookup"><span data-stu-id="8da44-152">Examples are HTTP (HyperText Transfer Protocol) and FTP (File Transfer Protocol).</span></span>

<span data-ttu-id="8da44-p113">ADO admite los proveedores OLE DB que reconocen sus propios esquemas URL. Por ejemplo, [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md),\*\* que obtiene acceso a los archivos "publicados" de Windows 2000, reconoce el esquema HTTP existente.</span><span class="sxs-lookup"><span data-stu-id="8da44-p113">ADO supports OLE DB providers that recognize their own URL schemes. For example, the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses "published" Windows 2000 files, recognizes the existing HTTP scheme.</span></span>

