---
title: Propiedad Connection.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e44ce5b4acf58f3f9d9e887d0136baed64c8e227
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295929"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="11bf7-102">Propiedad Connection.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="11bf7-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="11bf7-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="11bf7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="11bf7-104">Establece o devuelve un valor que proporciona información acerca del origen de una conexión abierta.</span><span class="sxs-lookup"><span data-stu-id="11bf7-104">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="11bf7-105">**String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="11bf7-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11bf7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11bf7-106">Syntax</span></span>

<span data-ttu-id="11bf7-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="11bf7-107">*expression* .Connect</span></span>

<span data-ttu-id="11bf7-108">*expression* Variable que representa un objeto **Connection**.</span><span class="sxs-lookup"><span data-stu-id="11bf7-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="11bf7-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="11bf7-109">Remarks</span></span>

<span data-ttu-id="11bf7-p102">El valor de la propiedad **Connect** es un valor de tipo **String** formado por un especificador de tipo de base de datos y cero o más parámetros separados por puntos y coma. La propiedad **Connect** pasa información adicional a controladores ODBC y algunos controladores ISAM, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="11bf7-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="11bf7-112">Para realizar una consulta SQL de paso a través en una tabla vinculada al archivo de base de datos de Microsoft Access, primero debe establecer la propiedad **Connect** de la base de datos de la tabla vinculada en una cadena de conexión ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="11bf7-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="11bf7-113">Para un objeto **TableDef** que representa una tabla vinculada, el valor de la propiedad **Connect** consta de una o dos partes (un especificador de tipo de base de datos y una ruta de acceso a la base de datos), con un punto y coma al final de cada una.</span><span class="sxs-lookup"><span data-stu-id="11bf7-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="11bf7-114">La ruta de acceso que se muestra en la siguiente tabla es la ruta completa del directorio que contiene los archivos de base de datos y debe ir precedida del identificador DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="11bf7-114">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="11bf7-115">En algunos casos (como en Microsoft Excel y en la base de datos del motor de bases de datos de Microsoft Access), debe incluir un nombre de archivo específico en el argumento rutaDeAccesso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="11bf7-115">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="11bf7-116">En la siguiente tabla se muestran los tipos de base de datos posibles así como sus especificadores de base de datos y rutas de acceso correspondientes para el valor de la propiedad **Connect**.</span><span class="sxs-lookup"><span data-stu-id="11bf7-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="11bf7-117">Tipo de base de datos</span><span class="sxs-lookup"><span data-stu-id="11bf7-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="11bf7-118">Especificador</span><span class="sxs-lookup"><span data-stu-id="11bf7-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="11bf7-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="11bf7-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-120">Base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="11bf7-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="11bf7-121">[database];</span><span class="sxs-lookup"><span data-stu-id="11bf7-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="11bf7-122">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="11bf7-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="11bf7-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="11bf7-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="11bf7-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-125">drive:\path</span><span class="sxs-lookup"><span data-stu-id="11bf7-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="11bf7-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="11bf7-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="11bf7-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-128">drive:\path</span><span class="sxs-lookup"><span data-stu-id="11bf7-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="11bf7-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="11bf7-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="11bf7-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-131">drive:\path</span><span class="sxs-lookup"><span data-stu-id="11bf7-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="11bf7-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="11bf7-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="11bf7-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-134">drive:\path</span><span class="sxs-lookup"><span data-stu-id="11bf7-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="11bf7-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="11bf7-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="11bf7-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-137">drive:\path</span><span class="sxs-lookup"><span data-stu-id="11bf7-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="11bf7-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="11bf7-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="11bf7-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-140">drive:\path</span><span class="sxs-lookup"><span data-stu-id="11bf7-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="11bf7-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="11bf7-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="11bf7-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-143">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="11bf7-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="11bf7-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="11bf7-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="11bf7-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-146">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="11bf7-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-147">Microsoft Excel 5.0 o Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="11bf7-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="11bf7-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="11bf7-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-149">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="11bf7-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="11bf7-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="11bf7-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="11bf7-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-152">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="11bf7-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-153">Lotus 1-2-3 WKS y WK1</span><span class="sxs-lookup"><span data-stu-id="11bf7-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="11bf7-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="11bf7-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-155">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="11bf7-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="11bf7-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="11bf7-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="11bf7-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-158">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="11bf7-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="11bf7-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="11bf7-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="11bf7-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-161">drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="11bf7-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-162">Importación HTML</span><span class="sxs-lookup"><span data-stu-id="11bf7-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="11bf7-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="11bf7-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-164">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="11bf7-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-165">Exportación HTML</span><span class="sxs-lookup"><span data-stu-id="11bf7-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="11bf7-166">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="11bf7-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-167">drive:\path</span><span class="sxs-lookup"><span data-stu-id="11bf7-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-168">Text</span><span class="sxs-lookup"><span data-stu-id="11bf7-168">Text</span></span></p></td>
<td><p><span data-ttu-id="11bf7-169">Text;</span><span class="sxs-lookup"><span data-stu-id="11bf7-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="11bf7-170">drive:\path</span><span class="sxs-lookup"><span data-stu-id="11bf7-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11bf7-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="11bf7-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="11bf7-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="11bf7-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="11bf7-173">Ninguna</span><span class="sxs-lookup"><span data-stu-id="11bf7-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11bf7-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="11bf7-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="11bf7-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="11bf7-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="11bf7-176">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="11bf7-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="11bf7-177">Si el especificador es sólo "ODBC;", el controlador ODBC muestra un cuadro de diálogo en el que se enumeran todos los nombres de orígenes de datos ODBC registrados para que el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="11bf7-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="11bf7-178">Si se necesita una contraseña pero ésta no se proporciona en el valor de la propiedad **Connect**, aparecerá un cuadro de diálogo de inicio de sesión la primera vez que el controlador de ODBC tenga acceso a una tabla y aparecerá otra vez si la conexión se cierra y se vuelve a abrir.</span><span class="sxs-lookup"><span data-stu-id="11bf7-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="11bf7-179">Para los datos de Microsoft Exchange, la clave requerida MAPILEVEL debe establecerse en una ruta de acceso de carpeta totalmente resuelta (por ejemplo, "Buzón - Almudena BenitoIAlpha/Hoy").</span><span class="sxs-lookup"><span data-stu-id="11bf7-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="11bf7-180">La ruta de acceso no incluye el nombre de la carpeta que se abrirá como una tabla; en cambio, ese nombre de carpeta debe estar especificado como argumento name para el método **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="11bf7-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="11bf7-181">La clave TABLETYPE debe estar establecida en "0" para abrir una carpeta (forma predeterminada) o en "1" para abrir una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="11bf7-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="11bf7-182">La clave PROFILE utiliza como valor predeterminado el perfil que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="11bf7-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="11bf7-183">Para las tablas base de una base de datos de Microsoft Access, el valor de la propiedad **Connect** es una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="11bf7-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="11bf7-184">Puede establecer la propiedad **Connect** de un objeto **Database** proporcionando un argumento source al método **OpenDatabase**.</span><span class="sxs-lookup"><span data-stu-id="11bf7-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="11bf7-185">Puede comprobar el valor para determinar el tipo, ruta de acceso, Id. de usuario, contraseña u origen de datos ODBC de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="11bf7-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="11bf7-186">En un objeto **QueryDef** de un área de trabajo de Microsoft Access, puede usar la propiedad **Connect** con la propiedad ReturnsRecords para crear una consulta SQL de paso a través de ODBC.</span><span class="sxs-lookup"><span data-stu-id="11bf7-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="11bf7-187">El argumento databasetype de la cadena de conexión es "ODBC;" y el resto de la cadena contiene información específica del controlador ODBC que se utiliza para tener acceso a los datos remotos.</span><span class="sxs-lookup"><span data-stu-id="11bf7-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="11bf7-188">Si desea más información, vea la documentación para el controlador específico.</span><span class="sxs-lookup"><span data-stu-id="11bf7-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="11bf7-189">Debe establecer la propiedad **Connect** antes de establecer la propiedad **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="11bf7-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="11bf7-190">Debe tener permisos de acceso al equipo que contiene el servidor de bases de datos al que intenta tener acceso.</span><span class="sxs-lookup"><span data-stu-id="11bf7-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


