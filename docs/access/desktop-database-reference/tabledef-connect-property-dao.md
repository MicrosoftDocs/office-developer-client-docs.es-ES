---
title: TableDef.Connect Property (DAO)
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
ms.openlocfilehash: eaedb53c8cb70746229e3f311ba5925e3b30ddef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/09/2018
ms.locfileid: "25485172"
---
# <a name="tabledefconnect-property-dao"></a><span data-ttu-id="40d46-102">TableDef.Connect Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="40d46-102">TableDef.Connect Property (DAO)</span></span>


<span data-ttu-id="40d46-103">**Se aplica a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="40d46-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="40d46-p101">Establece o devuelve un valor que proporciona información sobre una tabla vinculada. **String** de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="40d46-p101">Sets or returns a value that provides information about a linked table. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="40d46-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40d46-106">Syntax</span></span>

<span data-ttu-id="40d46-107">*expresión* . Conectar</span><span class="sxs-lookup"><span data-stu-id="40d46-107">*expression* .Connect</span></span>

<span data-ttu-id="40d46-108">*expresión* Variable que representa un objeto **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="40d46-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="40d46-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="40d46-109">Remarks</span></span>

<span data-ttu-id="40d46-p102">El valor de la propiedad **Connect** es un valor de tipo **String** formado por un especificador de tipo de base de datos y cero o más parámetros separados por puntos y coma. La propiedad **Connect** pasa información adicional a controladores ODBC y algunos controladores ISAM, según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="40d46-p102">The **Connect** property setting is a **String** composed of a database type specifier and zero or more parameters separated by semicolons. The **Connect** property passes additional information to ODBC and certain ISAM drivers as needed.</span></span>

<span data-ttu-id="40d46-112">Para un objeto **TableDef** que representa una tabla vinculada, el valor de la propiedad **Connect** consta de una o dos partes (un especificador de tipo de base de datos y una ruta de acceso a la base de datos), con un punto y coma al final de cada una.</span><span class="sxs-lookup"><span data-stu-id="40d46-112">For a **TableDef** object that represents a linked table, the **Connect** property setting consists of one or two parts (a database type specifier and a path to the database), each of which ends with a semicolon.</span></span>

<span data-ttu-id="40d46-p103">La ruta de acceso que se muestra en la siguiente tabla es la ruta completa del directorio que contiene los archivos de base de datos y debe ir precedida del identificador DATABASE=. En algunos casos (por ejemplo, con bases de datos de Microsoft Excel y del motor de base de datos de Microsoft Access), debe incluir un nombre de archivo específico en el argumento de ruta de acceso de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="40d46-p103">The path as shown in the following table is the full path for the directory containing the database files and must be preceded by the identifier DATABASE=. In some cases (as with Microsoft Excel and Microsoft Access database engine databases), you should include a specific file name in the database path argument.</span></span>

<span data-ttu-id="40d46-115">En la siguiente tabla se muestran los tipos de base de datos posibles así como sus especificadores de base de datos y rutas de acceso correspondientes para el valor de la propiedad **Connect**.</span><span class="sxs-lookup"><span data-stu-id="40d46-115">The following table shows possible database types and their corresponding database specifiers and paths for the **Connect** property setting.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="40d46-116">Tipo de base de datos</span><span class="sxs-lookup"><span data-stu-id="40d46-116">Database type</span></span></p></th>
<th><p><span data-ttu-id="40d46-117">Especificador</span><span class="sxs-lookup"><span data-stu-id="40d46-117">Specifier</span></span></p></th>
<th><p><span data-ttu-id="40d46-118">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40d46-118">Example</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="40d46-119">Base de datos de Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="40d46-119">Microsoft Access Database</span></span></p></td>
<td><p><span data-ttu-id="40d46-120">[base de datos;]</span><span class="sxs-lookup"><span data-stu-id="40d46-120">[database];</span></span></p></td>
<td><p><span data-ttu-id="40d46-121">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="40d46-121">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-122">dBASE III</span><span class="sxs-lookup"><span data-stu-id="40d46-122">dBASE III</span></span></p></td>
<td><p><span data-ttu-id="40d46-123">dBASE III;</span><span class="sxs-lookup"><span data-stu-id="40d46-123">dBASE III;</span></span></p></td>
<td><p><span data-ttu-id="40d46-124">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="40d46-124">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-125">dBASE IV</span><span class="sxs-lookup"><span data-stu-id="40d46-125">dBASE IV</span></span></p></td>
<td><p><span data-ttu-id="40d46-126">dBASE IV;</span><span class="sxs-lookup"><span data-stu-id="40d46-126">dBASE IV;</span></span></p></td>
<td><p><span data-ttu-id="40d46-127">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="40d46-127">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-128">dBASE 5</span><span class="sxs-lookup"><span data-stu-id="40d46-128">dBASE 5</span></span></p></td>
<td><p><span data-ttu-id="40d46-129">dBASE 5.0;</span><span class="sxs-lookup"><span data-stu-id="40d46-129">dBASE 5.0;</span></span></p></td>
<td><p><span data-ttu-id="40d46-130">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="40d46-130">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-131">Paradox 3.x</span><span class="sxs-lookup"><span data-stu-id="40d46-131">Paradox 3.x</span></span></p></td>
<td><p><span data-ttu-id="40d46-132">Paradox 3.x;</span><span class="sxs-lookup"><span data-stu-id="40d46-132">Paradox 3.x;</span></span></p></td>
<td><p><span data-ttu-id="40d46-133">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="40d46-133">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-134">Paradox 4.x</span><span class="sxs-lookup"><span data-stu-id="40d46-134">Paradox 4.x</span></span></p></td>
<td><p><span data-ttu-id="40d46-135">Paradox 4.x;</span><span class="sxs-lookup"><span data-stu-id="40d46-135">Paradox 4.x;</span></span></p></td>
<td><p><span data-ttu-id="40d46-136">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="40d46-136">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-137">Paradox 5.x</span><span class="sxs-lookup"><span data-stu-id="40d46-137">Paradox 5.x</span></span></p></td>
<td><p><span data-ttu-id="40d46-138">Paradox 5.x;</span><span class="sxs-lookup"><span data-stu-id="40d46-138">Paradox 5.x;</span></span></p></td>
<td><p><span data-ttu-id="40d46-139">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="40d46-139">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-140">Microsoft Excel 3.0</span><span class="sxs-lookup"><span data-stu-id="40d46-140">Microsoft Excel 3.0</span></span></p></td>
<td><p><span data-ttu-id="40d46-141">Excel 3.0;</span><span class="sxs-lookup"><span data-stu-id="40d46-141">Excel 3.0;</span></span></p></td>
<td><p><span data-ttu-id="40d46-142">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="40d46-142">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-143">Microsoft Excel 4.0</span><span class="sxs-lookup"><span data-stu-id="40d46-143">Microsoft Excel 4.0</span></span></p></td>
<td><p><span data-ttu-id="40d46-144">Excel 4.0;</span><span class="sxs-lookup"><span data-stu-id="40d46-144">Excel 4.0;</span></span></p></td>
<td><p><span data-ttu-id="40d46-145">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="40d46-145">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-146">Microsoft Excel 5.0 o Microsoft Excel 95</span><span class="sxs-lookup"><span data-stu-id="40d46-146">Microsoft Excel 5.0 or Microsoft Excel 95</span></span></p></td>
<td><p><span data-ttu-id="40d46-147">Excel 5.0;</span><span class="sxs-lookup"><span data-stu-id="40d46-147">Excel 5.0;</span></span></p></td>
<td><p><span data-ttu-id="40d46-148">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="40d46-148">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-149">Microsoft Excel 97</span><span class="sxs-lookup"><span data-stu-id="40d46-149">Microsoft Excel 97</span></span></p></td>
<td><p><span data-ttu-id="40d46-150">Excel 8.0;</span><span class="sxs-lookup"><span data-stu-id="40d46-150">Excel 8.0;</span></span></p></td>
<td><p><span data-ttu-id="40d46-151">Drive:\path\filename.xls</span><span class="sxs-lookup"><span data-stu-id="40d46-151">drive:\path\filename.xls</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-152">Lotus 1-2-3 WKS y WK1</span><span class="sxs-lookup"><span data-stu-id="40d46-152">Lotus 1-2-3 WKS and WK1</span></span></p></td>
<td><p><span data-ttu-id="40d46-153">Lotus WK1;</span><span class="sxs-lookup"><span data-stu-id="40d46-153">Lotus WK1;</span></span></p></td>
<td><p><span data-ttu-id="40d46-154">Drive:\path\filename.wk1</span><span class="sxs-lookup"><span data-stu-id="40d46-154">drive:\path\filename.wk1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-155">Lotus 1-2-3 WK3</span><span class="sxs-lookup"><span data-stu-id="40d46-155">Lotus 1-2-3 WK3</span></span></p></td>
<td><p><span data-ttu-id="40d46-156">Lotus WK3;</span><span class="sxs-lookup"><span data-stu-id="40d46-156">Lotus WK3;</span></span></p></td>
<td><p><span data-ttu-id="40d46-157">Drive:\path\filename.wk3</span><span class="sxs-lookup"><span data-stu-id="40d46-157">drive:\path\filename.wk3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-158">Lotus 1-2-3 WK4</span><span class="sxs-lookup"><span data-stu-id="40d46-158">Lotus 1-2-3 WK4</span></span></p></td>
<td><p><span data-ttu-id="40d46-159">Lotus WK4;</span><span class="sxs-lookup"><span data-stu-id="40d46-159">Lotus WK4;</span></span></p></td>
<td><p><span data-ttu-id="40d46-160">Drive:\path\filename.wk4</span><span class="sxs-lookup"><span data-stu-id="40d46-160">drive:\path\filename.wk4</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-161">Importación HTML</span><span class="sxs-lookup"><span data-stu-id="40d46-161">HTML Import</span></span></p></td>
<td><p><span data-ttu-id="40d46-162">HTML Import;</span><span class="sxs-lookup"><span data-stu-id="40d46-162">HTML Import;</span></span></p></td>
<td><p><span data-ttu-id="40d46-163">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="40d46-163">drive:\path\filename</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-164">Exportación HTML</span><span class="sxs-lookup"><span data-stu-id="40d46-164">HTML Export</span></span></p></td>
<td><p><span data-ttu-id="40d46-165">HTML Export;</span><span class="sxs-lookup"><span data-stu-id="40d46-165">HTML Export;</span></span></p></td>
<td><p><span data-ttu-id="40d46-166">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="40d46-166">drive:\path</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-167">Texto</span><span class="sxs-lookup"><span data-stu-id="40d46-167">Text</span></span></p></td>
<td><p><span data-ttu-id="40d46-168">Text;</span><span class="sxs-lookup"><span data-stu-id="40d46-168">Text;</span></span></p></td>
<td><p><span data-ttu-id="40d46-169">unidad: \path</span><span class="sxs-lookup"><span data-stu-id="40d46-169">drive:\path</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="40d46-170">ODBC</span><span class="sxs-lookup"><span data-stu-id="40d46-170">ODBC</span></span></p></td>
<td><p><span data-ttu-id="40d46-171">ODBC; Base de datos = base de datos; UID = usuario; PWD = contraseña; DSN = datasourcename; [LOGINTIMEOUT = segundos;]</span><span class="sxs-lookup"><span data-stu-id="40d46-171">ODBC; DATABASE=database; UID=user; PWD=password; DSN= datasourcename; [LOGINTIMEOUT=seconds;]</span></span></p></td>
<td><p><span data-ttu-id="40d46-172">Ninguno</span><span class="sxs-lookup"><span data-stu-id="40d46-172">None</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="40d46-173">Microsoft Exchange</span><span class="sxs-lookup"><span data-stu-id="40d46-173">Microsoft Exchange</span></span></p></td>
<td><p><span data-ttu-id="40d46-174">Exchange 4.0; MAPILEVEL = folderpath; [TABLETYPE = {0 | 1}]; [PROFILE = perfil;] [PWD = contraseña;] [Base de datos = base de datos;]</span><span class="sxs-lookup"><span data-stu-id="40d46-174">Exchange 4.0; MAPILEVEL=folderpath; [TABLETYPE={ 0 | 1 }];[PROFILE=profile;] [PWD=password;] [DATABASE=database;]</span></span></p></td>
<td><p><span data-ttu-id="40d46-175">unidad:\ruta de acceso\nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="40d46-175">drive:\path\filename</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="40d46-176">Si se requiere una contraseña pero no se proporciona en el valor de la propiedad **Connect**, se muestra un cuadro de diálogo de inicio de sesión la primera vez que el controlador ODBC obtiene acceso a una tabla y, de nuevo, si la conexión se cierra y se vuelve a abrir.</span><span class="sxs-lookup"><span data-stu-id="40d46-176">If a password is required but not provided in the **Connect** property setting, a login dialog box is displayed the first time a table is accessed by the ODBC driver and again if the connection is closed and reopened.</span></span>

<span data-ttu-id="40d46-177">Para los datos de Microsoft Exchange, la clave MAPILEVEL requerida debe establecerse en una ruta de acceso completa resuelta a una carpeta (por ejemplo, "Buzón - Almudena BenitoIAlpha/Hoy").</span><span class="sxs-lookup"><span data-stu-id="40d46-177">For data in Microsoft Exchange, the required MAPILEVEL key should be set to a fully-resolved folder path (for example, "Mailbox - Pat SmithIAlpha/Today").</span></span> <span data-ttu-id="40d46-178">La ruta de acceso no incluye el nombre de la carpeta que se va a abrir como una tabla; nombre de la carpeta en su lugar, debe especificarse como el argumento de nombre para el método **CreateTable** .</span><span class="sxs-lookup"><span data-stu-id="40d46-178">The path does not include the name of the folder that will be opened as a table; that folder’s name should instead be specified as the name argument to the **CreateTable** method.</span></span> <span data-ttu-id="40d46-179">La clave TABLETYPE debe establecerse en "0" para abrir una carpeta (valor predeterminado) o en "1" para abrir una libreta de direcciones.</span><span class="sxs-lookup"><span data-stu-id="40d46-179">The TABLETYPE key should be set to "0" to open a folder (default) or "1" to open an address book.</span></span> <span data-ttu-id="40d46-180">El valor predeterminado de la clave PROFILE es el perfil actualmente en uso.</span><span class="sxs-lookup"><span data-stu-id="40d46-180">The PROFILE key defaults to the profile currently in use.</span></span>

<span data-ttu-id="40d46-181">Para las tablas base de una base de datos de Microsoft Access, el valor de la propiedad **Connect** es una cadena de longitud cero ("").</span><span class="sxs-lookup"><span data-stu-id="40d46-181">For base tables in a Micorosoft Access database, the **Connect** property setting is a zero-length string ("").</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="40d46-182">Debe establecer la propiedad <STRONG>Connect</STRONG> antes de establecer la propiedad <STRONG>ReturnsRecords</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="40d46-182">You must set the <STRONG>Connect</STRONG> property before you set the <STRONG>ReturnsRecords</STRONG> property.</span></span></P>
> <LI>
> <P><span data-ttu-id="40d46-183">Debe tener permisos de acceso al equipo que contiene el servidor de base de datos al que intenta obtener acceso.</span><span class="sxs-lookup"><span data-stu-id="40d46-183">You must have access permissions to the computer that contains the database server you're trying to access.</span></span></P></LI></UL>

