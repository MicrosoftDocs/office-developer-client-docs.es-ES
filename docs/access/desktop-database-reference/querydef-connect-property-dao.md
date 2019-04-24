---
title: Propiedad QueryDef. Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 14f19205-e92e-acc6-5677-b6d88772d5da
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845479(v=office.15)
ms:contentKeyID: 48543398
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 009e49a96ea1cd5ee3db0b96adb9cae4a6bce21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301088"
---
# <a name="querydefconnect-property-dao"></a><span data-ttu-id="29497-102">Propiedad QueryDef. Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="29497-102">QueryDef.Connect property (DAO)</span></span>

<span data-ttu-id="29497-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="29497-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="29497-104">Establece o devuelve un valor que proporciona información sobre el origen de la base de datos utilizada en una consulta de paso a través.</span><span class="sxs-lookup"><span data-stu-id="29497-104">Sets or returns a value that provides information about the source of database used in a pass-through query.</span></span> <span data-ttu-id="29497-105">**String** de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="29497-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="29497-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29497-106">Syntax</span></span>

<span data-ttu-id="29497-107">*expresión* . A</span><span class="sxs-lookup"><span data-stu-id="29497-107">*expression* .Connect</span></span>

<span data-ttu-id="29497-108">*expresión* Variable que representa un objeto **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="29497-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="29497-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="29497-109">Remarks</span></span>

<span data-ttu-id="29497-p102">El valor de la propiedad **Connect** es una **String** compuesta por una de base de datos tipo especificadora y cero o más parámetros separados por punto y coma. La propiedad **Connect** pasa información adicional a ODBC y a algunos controladores ISAM, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="29497-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="29497-112">Para realizar una consulta SQL de paso a través en una tabla vinculada a su archivo de base de datos de Microsoft Access, primero debe establecer la propiedad **Connect** de la base de datos de la tabla vinculada en una cadena de conexión ODBC válida.</span><span class="sxs-lookup"><span data-stu-id="29497-112">To perform an SQL pass-through query on a table linked to your Microsoft Access database file, you must first set the **Connect** property of the linked table's database to a valid ODBC connection string.</span></span>

<span data-ttu-id="29497-113">La ruta de acceso que se muestra en la siguiente tabla es la ruta completa del directorio que contiene los archivos de base de datos y debe ir precedida del identificador DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="29497-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="29497-114">En algunos casos (como en Microsoft Excel y en la base de datos del motor de bases de datos de Microsoft Access), debe incluir un nombre de archivo específico en el argumento rutaDeAccesso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="29497-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="29497-115">En la siguiente tabla se muestran los tipos de base de datos posibles así como sus especificadores de base de datos y rutas de acceso correspondientes para el valor de la propiedad **Connect**.</span><span class="sxs-lookup"><span data-stu-id="29497-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="29497-116">Tipo de base de datos</span><span class="sxs-lookup"><span data-stu-id="29497-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="29497-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="29497-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="29497-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29497-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="29497-119">Base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="29497-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="29497-120">[base de datos];</span><span class="sxs-lookup"><span data-stu-id="29497-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="29497-121">unidad: \ path\filename</span><span class="sxs-lookup"><span data-stu-id="29497-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="29497-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="29497-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="29497-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="29497-124">unidad: \ rutaDeAcceso</span><span class="sxs-lookup"><span data-stu-id="29497-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="29497-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="29497-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="29497-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="29497-127">unidad: \ rutaDeAcceso</span><span class="sxs-lookup"><span data-stu-id="29497-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="29497-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="29497-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="29497-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="29497-130">unidad: \ rutaDeAcceso</span><span class="sxs-lookup"><span data-stu-id="29497-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="29497-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="29497-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="29497-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="29497-133">unidad: \ rutaDeAcceso</span><span class="sxs-lookup"><span data-stu-id="29497-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="29497-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="29497-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="29497-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="29497-136">unidad: \ rutaDeAcceso</span><span class="sxs-lookup"><span data-stu-id="29497-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="29497-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="29497-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="29497-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="29497-139">unidad: \ rutaDeAcceso</span><span class="sxs-lookup"><span data-stu-id="29497-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="29497-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="29497-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="29497-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="29497-142">unidad: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="29497-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="29497-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="29497-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="29497-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="29497-145">unidad: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="29497-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-146">Microsoft Excel 5.0 o Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="29497-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="29497-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="29497-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="29497-148">unidad: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="29497-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="29497-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="29497-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="29497-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="29497-151">unidad: \ path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="29497-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-152">Lotus 1-2-3 WKS y WK1</span><span class="sxs-lookup"><span data-stu-id="29497-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="29497-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="29497-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="29497-154">unidad: \ path\filename.WK1</span><span class="sxs-lookup"><span data-stu-id="29497-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="29497-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="29497-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="29497-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="29497-157">unidad: \ path\filename.WK3</span><span class="sxs-lookup"><span data-stu-id="29497-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="29497-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="29497-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="29497-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="29497-160">unidad: \ path\filename.WK4</span><span class="sxs-lookup"><span data-stu-id="29497-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-161">Importación HTML</span><span class="sxs-lookup"><span data-stu-id="29497-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="29497-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="29497-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="29497-163">unidad: \ path\filename</span><span class="sxs-lookup"><span data-stu-id="29497-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-164">Exportación HTML</span><span class="sxs-lookup"><span data-stu-id="29497-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="29497-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="29497-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="29497-166">unidad: \ rutaDeAcceso</span><span class="sxs-lookup"><span data-stu-id="29497-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-167">Texto</span><span class="sxs-lookup"><span data-stu-id="29497-167">Text</span></span></p></td>
<td><p><span data-ttu-id="29497-168">Edición</span><span class="sxs-lookup"><span data-stu-id="29497-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="29497-169">unidad: \ rutaDeAcceso</span><span class="sxs-lookup"><span data-stu-id="29497-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="29497-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="29497-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="29497-171">ODBC DATABASE = base de datos; UID = usuario; PWD = contraseña; DSN = datasourcename; [LOGINTIMEOUT = segundos;]</span><span class="sxs-lookup"><span data-stu-id="29497-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="29497-172">Ninguno</span><span class="sxs-lookup"><span data-stu-id="29497-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="29497-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="29497-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="29497-174">Exchange 4,0; MAPILEVEL = folderPath; [TABLETYPE = {0 | 1}]; [PROFILE = perfil;] [PWD = contraseña;] [DATABASE = base de datos;]</span><span class="sxs-lookup"><span data-stu-id="29497-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="29497-175">unidad: \ path\filename</span><span class="sxs-lookup"><span data-stu-id="29497-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="29497-176">Si el especificador es sólo "ODBC;", el controlador ODBC muestra un cuadro de diálogo en el que se enumeran todos los nombres de orígenes de datos ODBC registrados para que el usuario pueda seleccionar una base de datos.</span><span class="sxs-lookup"><span data-stu-id="29497-176">If the specifier is only "ODBC;", the ODBC driver displays a dialog box listing all registered ODBC data source names so that the user can select a database.</span></span>

<span data-ttu-id="29497-177">Si se necesita una contraseña pero ésta no se proporciona en el valor de la propiedad **Connect**, aparecerá un cuadro de diálogo de inicio de sesión la primera vez que el controlador de ODBC tenga acceso a una tabla y aparecerá otra vez si la conexión se cierra y se vuelve a abrir.</span><span class="sxs-lookup"><span data-stu-id="29497-177">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="29497-178">Para los datos de Microsoft Exchange, la clave requerida MAPILEVEL debe establecerse en una ruta de acceso de carpeta totalmente resuelta (por ejemplo, "Buzón - Almudena BenitoIAlpha/Hoy").</span><span class="sxs-lookup"><span data-stu-id="29497-178">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="29497-179">La ruta de acceso no incluye el nombre de la carpeta que se abrirá como una tabla; en su lugar, el nombre de la carpeta debe especificarse como el argumento Name del método **createTable** .</span><span class="sxs-lookup"><span data-stu-id="29497-179">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="29497-180">La clave TABLETYPE debe estar establecida en "0" para abrir una carpeta (forma predeterminada) o en "1" para abrir una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="29497-180">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="29497-181">La clave PROFILE predetermina el perfil utilizado actualmente.</span><span class="sxs-lookup"><span data-stu-id="29497-181">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="29497-182">En un objeto **QueryDef** en un área de trabajo de Microsoft Access, puede utilizar la propiedad **Connect** con la propiedad ReturnsRecords para crear una consulta SQL de paso a través con ODBC.</span><span class="sxs-lookup"><span data-stu-id="29497-182">On a **QueryDef** object in a Microsoft Access workspace, you can use the **Connect** property with the ReturnsRecords property to create an ODBC SQL pass-through query.</span></span> <span data-ttu-id="29497-183">El argumento databasetype de la cadena de conexión es "ODBC;" y el resto de la cadena contiene información específica del controlador ODBC que se utiliza para tener acceso a los datos remotos.</span><span class="sxs-lookup"><span data-stu-id="29497-183">The databasetype of the connection string is "ODBC;", and the remainder of the string contains information specific to the ODBC driver used to access the remote data.</span></span> <span data-ttu-id="29497-184">Si desea más información, vea la documentación para el controlador específico.</span><span class="sxs-lookup"><span data-stu-id="29497-184">For more information, see the documentation for the specific driver.</span></span>

> [!NOTE]
> - <span data-ttu-id="29497-185">Debe establecer la propiedad **Connect** antes de establecer la propiedad **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="29497-185">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="29497-186">Debe tener permisos de acceso al equipo que contiene el servidor de bases de datos al que intenta tener acceso.</span><span class="sxs-lookup"><span data-stu-id="29497-186">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>


