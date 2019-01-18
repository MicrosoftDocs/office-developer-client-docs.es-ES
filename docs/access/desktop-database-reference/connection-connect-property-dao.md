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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: es-ES
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720194"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="02dae-102">Propiedad Connection.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="02dae-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="02dae-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="02dae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02dae-p101">Establece o devuelve un valor que proporciona información acerca del origen de una conexión abierta. **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="02dae-p101">Sets or returns a value that provides information about the source of an open connection. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="02dae-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02dae-106">Syntax</span></span>

<span data-ttu-id="02dae-107">*expresión* . Conectar</span><span class="sxs-lookup"><span data-stu-id="02dae-107">*expression* .Connect</span></span>

<span data-ttu-id="02dae-108">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="02dae-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="02dae-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="02dae-109">Remarks</span></span>

<span data-ttu-id="02dae-p102">El valor de la propiedad **Connect** es una **String** compuesta por una de base de datos tipo especificadora y cero o más parámetros separados por punto y coma. La propiedad **Connect** pasa información adicional a ODBC y a algunos controladores ISAM, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="02dae-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="02dae-112">Para realizar una consulta SQL de paso a través en una tabla vinculada al archivo de base de datos de Microsoft Access, primero debe establecer la propiedad **Connect** de la base de datos de la tabla vinculada en una cadena de conexión ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="02dae-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="02dae-113">Para un objeto **TableDef** que representa una tabla vinculada, el valor de la propiedad **Connect** consta de dos partes (un especificador de tipo de base de datos y una ruta de acceso de la base de datos), cada una de las cuales termina con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="02dae-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="02dae-p103">La ruta de acceso que se muestra en la siguiente tabla es la ruta completa del directorio que contiene los archivos de base de datos y debe ir precedida del identificador DATABASE=. En algunos casos (por ejemplo, con bases de datos de Microsoft Excel y del motor de base de datos de Microsoft Access), debe incluir un nombre de archivo específico en el argumento de ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="02dae-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="02dae-116">En la siguiente tabla se muestran los tipos de base de datos posibles así como sus especificadores de base de datos y rutas de acceso correspondientes para el valor de la propiedad **Connect**.</span><span class="sxs-lookup"><span data-stu-id="02dae-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02dae-117">Tipo de base de datos</span><span class="sxs-lookup"><span data-stu-id="02dae-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="02dae-118">Especificador</span><span class="sxs-lookup"><span data-stu-id="02dae-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="02dae-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="02dae-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02dae-120">Base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="02dae-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="02dae-121">[base de datos;]</span><span class="sxs-lookup"><span data-stu-id="02dae-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="02dae-122">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="02dae-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="02dae-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="02dae-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="02dae-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="02dae-125">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="02dae-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="02dae-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="02dae-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="02dae-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="02dae-128">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="02dae-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="02dae-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="02dae-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="02dae-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="02dae-131">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="02dae-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="02dae-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="02dae-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="02dae-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="02dae-134">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="02dae-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="02dae-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="02dae-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="02dae-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="02dae-137">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="02dae-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="02dae-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="02dae-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="02dae-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="02dae-140">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="02dae-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="02dae-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="02dae-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="02dae-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="02dae-143">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="02dae-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="02dae-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="02dae-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="02dae-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="02dae-146">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="02dae-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-147">Microsoft Excel 5.0 o Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="02dae-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="02dae-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="02dae-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="02dae-149">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="02dae-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="02dae-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="02dae-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="02dae-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="02dae-152">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="02dae-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-153">Lotus 1-2-3 WKS y WK1</span><span class="sxs-lookup"><span data-stu-id="02dae-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="02dae-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="02dae-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="02dae-155">Drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="02dae-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="02dae-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="02dae-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="02dae-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="02dae-158">Drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="02dae-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="02dae-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="02dae-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="02dae-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="02dae-161">Drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="02dae-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-162">Importación HTML</span><span class="sxs-lookup"><span data-stu-id="02dae-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="02dae-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="02dae-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="02dae-164">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="02dae-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-165">Exportación HTML</span><span class="sxs-lookup"><span data-stu-id="02dae-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="02dae-166">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="02dae-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="02dae-167">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="02dae-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-168">Texto</span><span class="sxs-lookup"><span data-stu-id="02dae-168">Text</span></span></p></td>
<td><p><span data-ttu-id="02dae-169">Text;</span><span class="sxs-lookup"><span data-stu-id="02dae-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="02dae-170">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="02dae-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="02dae-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="02dae-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="02dae-172">ODBC; Base de datos = base de datos; UID = usuario; PWD = contraseña; DSN = datasourcename; [LOGINTIMEOUT = segundos;]</span><span class="sxs-lookup"><span data-stu-id="02dae-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="02dae-173">Ninguno</span><span class="sxs-lookup"><span data-stu-id="02dae-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="02dae-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="02dae-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="02dae-175">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = perfil;] [PWD = contraseña;] [Base de datos = base de datos;]</span><span class="sxs-lookup"><span data-stu-id="02dae-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="02dae-176">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="02dae-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="02dae-177">Si el especificador es sólo "ODBC;", el controlador ODBC muestra un cuadro de diálogo en el que se enumeran todos los nombres de orígenes de datos ODBC registrados para que el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="02dae-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="02dae-178">Si se requiere una contraseña pero no se proporciona en el valor de la propiedad **Connect**, se muestra un cuadro de diálogo de inicio de sesión la primera vez que el controlador ODBC obtiene acceso a una tabla y, de nuevo, si la conexión se cierra y se vuelve a abrir.</span><span class="sxs-lookup"><span data-stu-id="02dae-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="02dae-179">Para los datos de Microsoft Exchange, la clave MAPILEVEL requerida debe establecerse en una ruta de acceso completa resuelta a una carpeta (por ejemplo, "Buzón - Almudena BenitoIAlpha/Hoy").</span><span class="sxs-lookup"><span data-stu-id="02dae-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="02dae-180">La ruta de acceso no incluye el nombre de la carpeta que se va a abrir como una tabla; nombre de la carpeta en su lugar, debe especificarse como el argumento de nombre para el método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="02dae-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="02dae-181">La clave TABLETYPE debe establecerse en "0" para abrir una carpeta (valor predeterminado) o en "1" para abrir una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="02dae-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="02dae-182">El valor predeterminado de la clave PROFILE es el perfil actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="02dae-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="02dae-183">Para las tablas base de una base de datos de Microsoft Access, el valor de la propiedad **Connect** es una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="02dae-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="02dae-184">Puede establecer la propiedad **Connect** para un objeto de **base de datos** proporcionando un argumento source al método **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="02dae-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="02dae-185">Puede comprobar la configuración para determinar el tipo, ruta de acceso, identificador de usuario, contraseña u origen de datos ODBC de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="02dae-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="02dae-186">En un objeto **QueryDef** de un área de trabajo de Microsoft Access, puede usar la propiedad **Connect** con la propiedad ReturnsRecords para crear una consulta SQL de paso a través de ODBC.</span><span class="sxs-lookup"><span data-stu-id="02dae-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="02dae-187">El tipodebasededatos de la cadena de conexión es "ODBC;", y el resto de la cadena contiene información específica del controlador de ODBC utilizado para tener acceso a los datos remotos.</span><span class="sxs-lookup"><span data-stu-id="02dae-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="02dae-188">Si desea más información, vea la documentación para el controlador específico.</span><span class="sxs-lookup"><span data-stu-id="02dae-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="02dae-189">Debe establecer la propiedad **Connect** antes de establecer la propiedad **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="02dae-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="02dae-190">Debe tener permisos de acceso al equipo que contiene el servidor de base de datos al que intenta obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="02dae-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


