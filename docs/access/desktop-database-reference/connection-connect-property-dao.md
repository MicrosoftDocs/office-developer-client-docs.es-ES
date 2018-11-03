---
title: Propiedad Connection.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 58b514a2-91cd-7918-cba5-15d71c2457a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194335(v=office.15)
ms:contentKeyID: 48545001
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3a6c20ca3329edb64b79aa92c7598237c393bed5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931074"
---
# <a name="connectionconnect-property-dao"></a><span data-ttu-id="689ea-102">Propiedad Connection.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="689ea-102">Connection.Connect property (DAO)</span></span>


<span data-ttu-id="689ea-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="689ea-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="689ea-p101">Establece o devuelve un valor que proporciona información acerca del origen de una conexión abierta. **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="689ea-p101">Sets or returns a value that provides information about the source of an open connection. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="689ea-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="689ea-106">Syntax</span></span>

<span data-ttu-id="689ea-107">*expresión* . Conectar</span><span class="sxs-lookup"><span data-stu-id="689ea-107">*expression* .Connect</span></span>

<span data-ttu-id="689ea-108">*expresión* Variable que representa un objeto **Connection** .</span><span class="sxs-lookup"><span data-stu-id="689ea-108">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="689ea-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="689ea-109">Remarks</span></span>

<span data-ttu-id="689ea-p102">El valor de la propiedad **Connect** es una **String** compuesta por una de base de datos tipo especificadora y cero o más parámetros separados por punto y coma. La propiedad **Connect** pasa información adicional a ODBC y a algunos controladores ISAM, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="689ea-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="689ea-112">Para realizar una consulta SQL de paso a través en una tabla vinculada al archivo de base de datos de Microsoft Access, primero debe establecer la propiedad **Connect** de la base de datos de la tabla vinculada en una cadena de conexión ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="689ea-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="689ea-113">Para un objeto **TableDef** que representa una tabla vinculada, el valor de la propiedad **Connect** consta de dos partes (un especificador de tipo de base de datos y una ruta de acceso de la base de datos), cada una de las cuales termina con un punto y coma.</span><span class="sxs-lookup"><span data-stu-id="689ea-113">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="689ea-p103">La ruta de acceso que se muestra en la siguiente tabla es la ruta completa del directorio que contiene los archivos de base de datos y debe ir precedida del identificador DATABASE=. En algunos casos (por ejemplo, con bases de datos de Microsoft Excel y del motor de base de datos de Microsoft Access), debe incluir un nombre de archivo específico en el argumento de ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="689ea-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="689ea-116">En la siguiente tabla se muestran los tipos de base de datos posibles así como sus especificadores de base de datos y rutas de acceso correspondientes para el valor de la propiedad **Connect**.</span><span class="sxs-lookup"><span data-stu-id="689ea-116">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="689ea-117">Tipo de base de datos</span><span class="sxs-lookup"><span data-stu-id="689ea-117">Database type</span></span></p></th>
<th><p><span data-ttu-id="689ea-118">Especificador</span><span class="sxs-lookup"><span data-stu-id="689ea-118">Specifier</span></span></p></th>
<th><p><span data-ttu-id="689ea-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="689ea-119">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="689ea-120">Base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="689ea-120">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="689ea-121">[base de datos;]</span><span class="sxs-lookup"><span data-stu-id="689ea-121">[database];</span></span></p></td>
<td><p><span data-ttu-id="689ea-122">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="689ea-122">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-123">dBASE III</span><span class="sxs-lookup"><span data-stu-id="689ea-123">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="689ea-124">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="689ea-124">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="689ea-125">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="689ea-125">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-126">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="689ea-126">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="689ea-127">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="689ea-127">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="689ea-128">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="689ea-128">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-129">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="689ea-129">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="689ea-130">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="689ea-130">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="689ea-131">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="689ea-131">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-132">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="689ea-132">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="689ea-133">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="689ea-133">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="689ea-134">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="689ea-134">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-135">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="689ea-135">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="689ea-136">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="689ea-136">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="689ea-137">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="689ea-137">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-138">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="689ea-138">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="689ea-139">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="689ea-139">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="689ea-140">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="689ea-140">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-141">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="689ea-141">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="689ea-142">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="689ea-142">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="689ea-143">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="689ea-143">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-144">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="689ea-144">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="689ea-145">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="689ea-145">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="689ea-146">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="689ea-146">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-147">Microsoft Excel 5.0 o Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="689ea-147">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="689ea-148">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="689ea-148">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="689ea-149">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="689ea-149">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-150">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="689ea-150">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="689ea-151">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="689ea-151">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="689ea-152">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="689ea-152">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-153">Lotus 1-2-3 WKS y WK1</span><span class="sxs-lookup"><span data-stu-id="689ea-153">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="689ea-154">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="689ea-154">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="689ea-155">Drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="689ea-155">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-156">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="689ea-156">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="689ea-157">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="689ea-157">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="689ea-158">Drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="689ea-158">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-159">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="689ea-159">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="689ea-160">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="689ea-160">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="689ea-161">Drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="689ea-161">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-162">Importación HTML</span><span class="sxs-lookup"><span data-stu-id="689ea-162">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="689ea-163">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="689ea-163">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="689ea-164">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="689ea-164">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-165">Exportación HTML</span><span class="sxs-lookup"><span data-stu-id="689ea-165">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="689ea-166">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="689ea-166">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="689ea-167">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="689ea-167">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-168">Texto</span><span class="sxs-lookup"><span data-stu-id="689ea-168">Text</span></span></p></td>
<td><p><span data-ttu-id="689ea-169">Text;</span><span class="sxs-lookup"><span data-stu-id="689ea-169">Text;</span></span></p></td>
<td><p><span data-ttu-id="689ea-170">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="689ea-170">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="689ea-171">ODBC</span><span class="sxs-lookup"><span data-stu-id="689ea-171">ODBC</span></span></p></td>
<td><p><span data-ttu-id="689ea-172">ODBC; Base de datos = base de datos; UID = usuario; PWD = contraseña; DSN = datasourcename; [LOGINTIMEOUT = segundos;]</span><span class="sxs-lookup"><span data-stu-id="689ea-172">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="689ea-173">Ninguno</span><span class="sxs-lookup"><span data-stu-id="689ea-173">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="689ea-174">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="689ea-174">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="689ea-175">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = perfil;] [PWD = contraseña;] [Base de datos = base de datos;]</span><span class="sxs-lookup"><span data-stu-id="689ea-175">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="689ea-176">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="689ea-176">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="689ea-177">Si el especificador es sólo "ODBC;", el controlador ODBC muestra un cuadro de diálogo en el que se enumeran todos los nombres de orígenes de datos ODBC registrados para que el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="689ea-177">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="689ea-178">Si se requiere una contraseña pero no se proporciona en el valor de la propiedad **Connect**, se muestra un cuadro de diálogo de inicio de sesión la primera vez que el controlador ODBC obtiene acceso a una tabla y, de nuevo, si la conexión se cierra y se vuelve a abrir.</span><span class="sxs-lookup"><span data-stu-id="689ea-178">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="689ea-179">Para los datos de Microsoft Exchange, la clave MAPILEVEL requerida debe establecerse en una ruta de acceso completa resuelta a una carpeta (por ejemplo, "Buzón - Almudena BenitoIAlpha/Hoy").</span><span class="sxs-lookup"><span data-stu-id="689ea-179">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="689ea-180">La ruta de acceso no incluye el nombre de la carpeta que se va a abrir como una tabla; nombre de la carpeta en su lugar, debe especificarse como el argumento de nombre para el método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="689ea-180">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="689ea-181">La clave TABLETYPE debe establecerse en "0" para abrir una carpeta (valor predeterminado) o en "1" para abrir una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="689ea-181">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="689ea-182">El valor predeterminado de la clave PROFILE es el perfil actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="689ea-182">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="689ea-183">Para las tablas base de una base de datos de Microsoft Access, el valor de la propiedad **Connect** es una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="689ea-183">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

<span data-ttu-id="689ea-184">Puede establecer la propiedad **Connect** para un objeto de **base de datos** proporcionando un argumento source al método **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="689ea-184">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="689ea-185">Puede comprobar la configuración para determinar el tipo, ruta de acceso, identificador de usuario, contraseña u origen de datos ODBC de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="689ea-185">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>

<span data-ttu-id="689ea-186">En un objeto **QueryDef** de un área de trabajo de Microsoft Access, puede usar la propiedad **Connect** con la propiedad ReturnsRecords para crear una consulta SQL de paso a través de ODBC.</span><span class="sxs-lookup"><span data-stu-id="689ea-186">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="689ea-187">El tipodebasededatos de la cadena de conexión es "ODBC;", y el resto de la cadena contiene información específica del controlador de ODBC utilizado para tener acceso a los datos remotos.</span><span class="sxs-lookup"><span data-stu-id="689ea-187">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="689ea-188">Si desea más información, vea la documentación para el controlador específico.</span><span class="sxs-lookup"><span data-stu-id="689ea-188">For more information, see the documentation for the specific driver.</span></span>


> [!NOTE]
> - <span data-ttu-id="689ea-189">Debe establecer la propiedad **Connect** antes de establecer la propiedad **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="689ea-189">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="689ea-190">Debe tener permisos de acceso al equipo que contiene el servidor de base de datos al que intenta obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="689ea-190">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


