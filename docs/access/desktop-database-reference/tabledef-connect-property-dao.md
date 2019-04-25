---
title: Propiedad TableDef.Connect (DAO)
TOCTitle: Connect Property
ms:assetid: 4fbb324c-a358-8fad-60f2-fb8005cf74d9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193791(v=office.15)
ms:contentKeyID: 48544782
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053064
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 2d8aef3c8bdaac93bd84231b3098d98ee896a81f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314388"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="adaa6-102">Propiedad TableDef.Connect (DAO)</span><span class="sxs-lookup"><span data-stu-id="adaa6-102">TableDef.Connect property (DAO)</span></span>

<span data-ttu-id="adaa6-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="adaa6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adaa6-104">Establece o devuelve un valor que proporciona información sobre una tabla vinculada.</span><span class="sxs-lookup"><span data-stu-id="adaa6-104">Sets or returns a value that provides information about a linked table.</span></span> <span data-ttu-id="adaa6-105">**String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="adaa6-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="adaa6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="adaa6-106">Syntax</span></span>

<span data-ttu-id="adaa6-107">*expression* .Connect</span><span class="sxs-lookup"><span data-stu-id="adaa6-107">expression  . Connect</span></span>

<span data-ttu-id="adaa6-108">*expression* Variable que representa un objeto **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="adaa6-108">*expression*  A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="adaa6-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="adaa6-109">Remarks</span></span>

<span data-ttu-id="adaa6-p102">El valor de la propiedad **Connect** es un valor de tipo **String** formado por un especificador de tipo de base de datos y cero o más parámetros separados por puntos y coma. La propiedad **Connect** pasa información adicional a controladores ODBC y algunos controladores ISAM, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="adaa6-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="adaa6-112">Para un objeto **TableDef** que representa una tabla vinculada, el valor de la propiedad **Connect** consta de una o dos partes (un especificador de tipo de base de datos y una ruta de acceso a la base de datos), con un punto y coma al final de cada una.</span><span class="sxs-lookup"><span data-stu-id="adaa6-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="adaa6-113">La ruta de acceso que se muestra en la siguiente tabla es la ruta completa del directorio que contiene los archivos de base de datos y debe ir precedida del identificador DATABASE=.</span><span class="sxs-lookup"><span data-stu-id="adaa6-113">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=.</span></span> <span data-ttu-id="adaa6-114">En algunos casos (como en Microsoft Excel y en la base de datos del motor de bases de datos de Microsoft Access), debe incluir un nombre de archivo específico en el argumento rutaDeAccesso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="adaa6-114">In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="adaa6-115">En la siguiente tabla se muestran los tipos de base de datos posibles así como sus especificadores de base de datos y rutas de acceso correspondientes para el valor de la propiedad **Connect**.</span><span class="sxs-lookup"><span data-stu-id="adaa6-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adaa6-116">Tipo de base de datos</span><span class="sxs-lookup"><span data-stu-id="adaa6-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="adaa6-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="adaa6-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="adaa6-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="adaa6-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-119">Base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="adaa6-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="adaa6-120">[database];</span><span class="sxs-lookup"><span data-stu-id="adaa6-120">Database</span></span></p></td>
<td><p><span data-ttu-id="adaa6-121">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="adaa6-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="adaa6-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="adaa6-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="adaa6-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-124">drive:\path</span><span class="sxs-lookup"><span data-stu-id="adaa6-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="adaa6-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="adaa6-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="adaa6-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-127">drive:\path</span><span class="sxs-lookup"><span data-stu-id="adaa6-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="adaa6-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="adaa6-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="adaa6-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-130">drive:\path</span><span class="sxs-lookup"><span data-stu-id="adaa6-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="adaa6-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="adaa6-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="adaa6-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-133">drive:\path</span><span class="sxs-lookup"><span data-stu-id="adaa6-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="adaa6-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="adaa6-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="adaa6-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-136">drive:\path</span><span class="sxs-lookup"><span data-stu-id="adaa6-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="adaa6-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="adaa6-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="adaa6-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-139">drive:\path</span><span class="sxs-lookup"><span data-stu-id="adaa6-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="adaa6-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="adaa6-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="adaa6-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-142">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="adaa6-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="adaa6-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="adaa6-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="adaa6-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-145">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="adaa6-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-146">Microsoft Excel 5.0 o Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="adaa6-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="adaa6-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="adaa6-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-148">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="adaa6-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="adaa6-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="adaa6-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="adaa6-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-151">drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="adaa6-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-152">Lotus 1-2-3 WKS y WK1</span><span class="sxs-lookup"><span data-stu-id="adaa6-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="adaa6-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="adaa6-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-154">drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="adaa6-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="adaa6-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="adaa6-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="adaa6-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-157">drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="adaa6-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="adaa6-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="adaa6-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="adaa6-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-160">drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="adaa6-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-161">Importación HTML</span><span class="sxs-lookup"><span data-stu-id="adaa6-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="adaa6-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="adaa6-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-163">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="adaa6-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-164">Exportación HTML</span><span class="sxs-lookup"><span data-stu-id="adaa6-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="adaa6-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="adaa6-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="adaa6-166">drive:\path</span><span class="sxs-lookup"><span data-stu-id="adaa6-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-167">Text</span><span class="sxs-lookup"><span data-stu-id="adaa6-167">Text</span></span></p></td>
<td><p><span data-ttu-id="adaa6-168">Text;</span><span class="sxs-lookup"><span data-stu-id="adaa6-168">Text</span></span></p></td>
<td><p><span data-ttu-id="adaa6-169">drive:\path</span><span class="sxs-lookup"><span data-stu-id="adaa6-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adaa6-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="adaa6-170">ODBC Database</span></span></p></td>
<td><p><span data-ttu-id="adaa6-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span><span class="sxs-lookup"><span data-stu-id="adaa6-171">ODBC;
DATABASE=database;
UID=user;
PWD=password;
DSN= datasourcename;
[LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="adaa6-172">Ninguna</span><span class="sxs-lookup"><span data-stu-id="adaa6-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adaa6-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="adaa6-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="adaa6-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span><span class="sxs-lookup"><span data-stu-id="adaa6-174">Exchange 4.0;
MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;]
[PWD=password;]
[DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="adaa6-175">drive:\path\filename</span><span class="sxs-lookup"><span data-stu-id="adaa6-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adaa6-176">Si se necesita una contraseña pero ésta no se proporciona en el valor de la propiedad **Connect**, aparecerá un cuadro de diálogo de inicio de sesión la primera vez que el controlador de ODBC tenga acceso a una tabla y aparecerá otra vez si la conexión se cierra y se vuelve a abrir.</span><span class="sxs-lookup"><span data-stu-id="adaa6-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="adaa6-177">Para los datos de Microsoft Exchange, la clave requerida MAPILEVEL debe establecerse en una ruta de acceso de carpeta totalmente resuelta (por ejemplo, "Buzón - Almudena BenitoIAlpha/Hoy").</span><span class="sxs-lookup"><span data-stu-id="adaa6-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="adaa6-178">La ruta de acceso no incluye el nombre de la carpeta que se abrirá como una tabla; en cambio, ese nombre de carpeta debe estar especificado como argumento name para el método **CreateTable**.</span><span class="sxs-lookup"><span data-stu-id="adaa6-178">The path does not include the name of the folder that will be opened as a table; that folder's name should instead be specified as the  name argument to the **CreateTable** method.</span></span> <span data-ttu-id="adaa6-179">La clave TABLETYPE debe estar establecida en "0" para abrir una carpeta (forma predeterminada) o en "1" para abrir una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="adaa6-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="adaa6-180">La clave PROFILE utiliza como valor predeterminado el perfil que se está utilizando.</span><span class="sxs-lookup"><span data-stu-id="adaa6-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="adaa6-181">Para las tablas base de una base de datos de Microsoft Access, el valor de la propiedad **Connect** es una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="adaa6-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="adaa6-182">Debe establecer la propiedad **Connect** antes de establecer la propiedad **ReturnsRecords**.</span><span class="sxs-lookup"><span data-stu-id="adaa6-182">You must set the **Connect** property before you set the **ReturnsRecords** property.</span></span>
> - <span data-ttu-id="adaa6-183">Debe tener permisos de acceso al equipo que contiene el servidor de bases de datos al que intenta tener acceso.</span><span class="sxs-lookup"><span data-stu-id="adaa6-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span>
