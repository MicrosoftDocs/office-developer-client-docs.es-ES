---
title: Database.Connect Property (DAO)
TOCTitle: Connect Property
ms:assetid: c3e511a6-baef-3758-cfb1-3459b0b19cf3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823048(v=office.15)
ms:contentKeyID: 48547578
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b497e2859b265f5bb939fdd2b4913a54fdf2d170
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864203"
---
# <a name="databaseconnect-property-dao"></a><span data-ttu-id="ac2e9-102">Database.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="ac2e9-102">Database.Connect Property (DAO)</span></span>


<span data-ttu-id="ac2e9-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac2e9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ac2e9-p101">Establece o devuelve un valor que proporciona información acerca del origen de una base de datos abierta. **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-p101">Sets or returns a value that provides information about the source an open database. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac2e9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac2e9-106">Syntax</span></span>

<span data-ttu-id="ac2e9-107">*expresión* . Conectar</span><span class="sxs-lookup"><span data-stu-id="ac2e9-107">*expression* .Connect</span></span>

<span data-ttu-id="ac2e9-108">*expresión* Variable que representa un objeto de **base de datos** .</span><span class="sxs-lookup"><span data-stu-id="ac2e9-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac2e9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac2e9-109">Remarks</span></span>

<span data-ttu-id="ac2e9-p102">El valor de la propiedad **Connect** es una **String** compuesta por una de base de datos tipo especificadora y cero o más parámetros separados por punto y coma. La propiedad **Connect** pasa información adicional a ODBC y a algunos controladores ISAM, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="ac2e9-112">Para realizar una consulta SQL de paso a través en una tabla vinculada a su archivo de base de datos de Microsoft Access, primero debe establecer la propiedad **Connect** de la base de datos de la tabla vinculada en una cadena de conexión ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="ac2e9-p103">La ruta de acceso que se muestra en la siguiente tabla es la ruta completa del directorio que contiene los archivos de base de datos y debe ir precedida del identificador DATABASE=. En algunos casos (por ejemplo, con bases de datos de Microsoft Excel y del motor de base de datos de Microsoft Access), debe incluir un nombre de archivo específico en el argumento de ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="ac2e9-115">En la siguiente tabla se muestran los tipos de base de datos posibles así como sus especificadores de base de datos y rutas de acceso correspondientes para el valor de la propiedad **Connect**.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ac2e9-116">Tipo de base de datos</span><span class="sxs-lookup"><span data-stu-id="ac2e9-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="ac2e9-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="ac2e9-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="ac2e9-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac2e9-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-119">Base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="ac2e9-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-120">[base de datos;]</span><span class="sxs-lookup"><span data-stu-id="ac2e9-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-121">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="ac2e9-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="ac2e9-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-124">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="ac2e9-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="ac2e9-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-127">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="ac2e9-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="ac2e9-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-130">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="ac2e9-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="ac2e9-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-133">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="ac2e9-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="ac2e9-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-136">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="ac2e9-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="ac2e9-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-139">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="ac2e9-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="ac2e9-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-142">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="ac2e9-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="ac2e9-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-145">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="ac2e9-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-146">Microsoft Excel 5.0 o Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="ac2e9-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-148">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="ac2e9-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="ac2e9-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-151">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="ac2e9-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-152">Lotus 1-2-3 WKS y WK1</span><span class="sxs-lookup"><span data-stu-id="ac2e9-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-154">Drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="ac2e9-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="ac2e9-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-157">Drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="ac2e9-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="ac2e9-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-160">Drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="ac2e9-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-161">Importación HTML</span><span class="sxs-lookup"><span data-stu-id="ac2e9-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-163">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="ac2e9-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-164">Exportación HTML</span><span class="sxs-lookup"><span data-stu-id="ac2e9-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-166">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="ac2e9-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-167">Texto</span><span class="sxs-lookup"><span data-stu-id="ac2e9-167">Text</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-168">Text;</span><span class="sxs-lookup"><span data-stu-id="ac2e9-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-169">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="ac2e9-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ac2e9-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="ac2e9-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-171">ODBC; Base de datos = base de datos; UID = usuario; PWD = contraseña; DSN = datasourcename; [LOGINTIMEOUT = segundos;]</span><span class="sxs-lookup"><span data-stu-id="ac2e9-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-172">Ninguno</span><span class="sxs-lookup"><span data-stu-id="ac2e9-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ac2e9-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="ac2e9-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = perfil;] [PWD = contraseña;] [Base de datos = base de datos;]</span><span class="sxs-lookup"><span data-stu-id="ac2e9-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="ac2e9-175">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="ac2e9-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ac2e9-176">Si el especificador es sólo "ODBC;", el controlador ODBC muestra un cuadro de diálogo en el que se enumeran todos los nombres de orígenes de datos ODBC registrados para que el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="ac2e9-177">Si se requiere una contraseña pero no se proporciona en el valor de la propiedad **Connect**, se muestra un cuadro de diálogo de inicio de sesión la primera vez que el controlador ODBC obtiene acceso a una tabla y, de nuevo, si la conexión se cierra y se vuelve a abrir.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="ac2e9-178">Para los datos de Microsoft Exchange, la clave MAPILEVEL requerida debe establecerse en una ruta de acceso completa resuelta a una carpeta (por ejemplo, "Buzón - Almudena BenitoIAlpha/Hoy").</span><span class="sxs-lookup"><span data-stu-id="ac2e9-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="ac2e9-179">La ruta de acceso no incluye el nombre de la carpeta que se va a abrir como una tabla; nombre de la carpeta en su lugar, debe especificarse como el argumento de nombre para el método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="ac2e9-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="ac2e9-180">La clave TABLETYPE debe establecerse en "0" para abrir una carpeta (valor predeterminado) o en "1" para abrir una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="ac2e9-181">El valor predeterminado de la clave PROFILE es el perfil actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="ac2e9-182">Puede establecer la propiedad **Connect** para un objeto de **base de datos** proporcionando un argumento source al método **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="ac2e9-182">You can set the **Connect** property for a **Database** object by providing a source argument to the **OpenDatabase** method.</span></span> <span data-ttu-id="ac2e9-183">Puede comprobar la configuración para determinar el tipo, ruta de acceso, identificador de usuario, contraseña u origen de datos ODBC de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-183">You can check the setting to determine the type, path, user ID, password, or ODBC data source of the database.</span></span>


> [!NOTE]
> - <span data-ttu-id="ac2e9-184">La propiedad **Connect** debe establecerse antes que la propiedad **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-184">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="ac2e9-185">Debe tener permisos de acceso al equipo que contiene el servidor de base de datos al que intenta obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="ac2e9-185">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


