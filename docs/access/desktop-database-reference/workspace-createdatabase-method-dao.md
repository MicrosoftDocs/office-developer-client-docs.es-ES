---
title: Método Workspace. CreateDatabase (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: c0ad986e-3b4d-f781-f782-5aa3cdccea7d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822832(v=office.15)
ms:contentKeyID: 48547514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e6d271676ef91d29dca78ba9ee4b6142e055b36d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305869"
---
# <a name="workspacecreatedatabase-method-dao"></a><span data-ttu-id="fb6df-102">Método Workspace. CreateDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="fb6df-102">Workspace.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="fb6df-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fb6df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fb6df-104">Crea un nuevo objeto **[Database](database-object-dao.md)**, guarda la base de datos en el disco y devuelve un objeto **Database** abierto (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="fb6df-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6df-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb6df-105">Syntax</span></span>

<span data-ttu-id="fb6df-106">*expresión* . CreateDatabase (***Name***, ***Connect***, ***Option***)</span><span class="sxs-lookup"><span data-stu-id="fb6df-106">*expression* .CreateDatabase(***Name***, ***Connect***, ***Option***)</span></span>

<span data-ttu-id="fb6df-107">*expresión* Variable que representa un objeto **Workspace** .</span><span class="sxs-lookup"><span data-stu-id="fb6df-107">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="fb6df-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="fb6df-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb6df-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="fb6df-109">Name</span></span></p></th>
<th><p><span data-ttu-id="fb6df-110">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="fb6df-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="fb6df-111">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="fb6df-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="fb6df-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb6df-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="fb6df-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="fb6df-114">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fb6df-114">Required</span></span></p></td>
<td><p><span data-ttu-id="fb6df-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-116">String de hasta 255 caracteres de longitud que es el nombre del archivo de base de datos que va a crear.</span><span class="sxs-lookup"><span data-stu-id="fb6df-116">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="fb6df-117">Puede ser la ruta completa y el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="fb6df-117">It can be the full path and file name.</span></span> <span data-ttu-id="fb6df-118">Si la red lo admite, también puede especificar una ruta de acceso de red, &quot; \\como&quot;server1\share1\dir1\db1.</span><span class="sxs-lookup"><span data-stu-id="fb6df-118">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="fb6df-119">Con este método sólo puede crear archivos de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="fb6df-119">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-120"><em>Connect</em></span><span class="sxs-lookup"><span data-stu-id="fb6df-120"><em>Connect</em></span></span></p></td>
<td><p><span data-ttu-id="fb6df-121">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="fb6df-121">Required</span></span></p></td>
<td><p><span data-ttu-id="fb6df-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-122"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="fb6df-p102">Expresión de cadena que especifica un orden de intercalación para crear la base de datos, tal como se especifica en la sección de configuración. Debe proporcionar este argumento o se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="fb6df-p102">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="fb6df-125">También puede crear una contraseña para el nuevo objeto <strong>Database</strong> concatenando la cadena de contraseña (a partir de &quot;;p WD =&quot;) con una constante en el <em></em> argumento locale, como se muestra a continuación:</span><span class="sxs-lookup"><span data-stu-id="fb6df-125">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="fb6df-126">dbLangSpanish &amp; &quot;;p wd = nuevacontraseña&quot;</span><span class="sxs-lookup"><span data-stu-id="fb6df-126">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="fb6df-127">Si desea utilizar el argumento <em>locale</em> predeterminado, pero especificar una contraseña, sólo tiene que agregar una cadena de contraseña al argumento <em>locale</em>:</span><span class="sxs-lookup"><span data-stu-id="fb6df-127">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="fb6df-128">&quot;;p WD = nuevacontraseña&quot;</span><span class="sxs-lookup"><span data-stu-id="fb6df-128">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="fb6df-p103">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="fb6df-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-134"><em>Opción</em></span><span class="sxs-lookup"><span data-stu-id="fb6df-134"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="fb6df-135">Opcional</span><span class="sxs-lookup"><span data-stu-id="fb6df-135">Optional</span></span></p></td>
<td><p><span data-ttu-id="fb6df-136"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-136"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-p104">Constante o combinación de constantes que indican una o varias opciones, tal como se especifica en la sección de configuración. Puede combinar opciones sumando las constantes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="fb6df-p104">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="fb6df-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fb6df-139">Remarks</span></span>

<span data-ttu-id="fb6df-140">Puede utilizar alguna de las constantes siguientes para el argumento locale si desea especificar la propiedad [CollatingOrder](database-collatingorder-property-dao.md) de texto para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="fb6df-140">You can use one of the following constants for the locale argument to specify the [CollatingOrder](database-collatingorder-property-dao.md) property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb6df-141">Constante</span><span class="sxs-lookup"><span data-stu-id="fb6df-141">Constant</span></span></p></th>
<th><p><span data-ttu-id="fb6df-142">Orden de intercalación</span><span class="sxs-lookup"><span data-stu-id="fb6df-142">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-143"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-143"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-144">Inglés, alemán, francés, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="fb6df-144">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-145"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-145"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-146">Árabe</span><span class="sxs-lookup"><span data-stu-id="fb6df-146">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-147"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-147"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-148">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="fb6df-148">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-149"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-149"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-150">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="fb6df-150">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-151"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-151"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-152">Ruso</span><span class="sxs-lookup"><span data-stu-id="fb6df-152">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-153"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-153"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-154">Checo</span><span class="sxs-lookup"><span data-stu-id="fb6df-154">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-155"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-155"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-156">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="fb6df-156">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-157"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-157"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-158">Griego</span><span class="sxs-lookup"><span data-stu-id="fb6df-158">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-159"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-159"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-160">Hebreo</span><span class="sxs-lookup"><span data-stu-id="fb6df-160">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-161"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-161"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-162">Húngaro</span><span class="sxs-lookup"><span data-stu-id="fb6df-162">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-163"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-163"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-164">Islandés</span><span class="sxs-lookup"><span data-stu-id="fb6df-164">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-165"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-165"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-166">Japonés</span><span class="sxs-lookup"><span data-stu-id="fb6df-166">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-167"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-167"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-168">Coreano</span><span class="sxs-lookup"><span data-stu-id="fb6df-168">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-169"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-169"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-170">Idiomas nórdicos (sólo en la versión 1.0 del motor de base de datos de Microsoft Jet)</span><span class="sxs-lookup"><span data-stu-id="fb6df-170">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-171"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-171"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-172">Noruego y danés</span><span class="sxs-lookup"><span data-stu-id="fb6df-172">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-173"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-173"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-174">Polaco</span><span class="sxs-lookup"><span data-stu-id="fb6df-174">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-175"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-175"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-176">Esloveno</span><span class="sxs-lookup"><span data-stu-id="fb6df-176">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-177"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-177"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-178">Español (alfab. tradicional)</span><span class="sxs-lookup"><span data-stu-id="fb6df-178">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-179"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-179"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-180">Sueco y finlandés</span><span class="sxs-lookup"><span data-stu-id="fb6df-180">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-181"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-181"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-182">Tailandés</span><span class="sxs-lookup"><span data-stu-id="fb6df-182">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-183"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-183"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-184">Turco</span><span class="sxs-lookup"><span data-stu-id="fb6df-184">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="fb6df-185">Puede utilizar una o varias de las constantes siguientes en el argumento options para especificar la versión que debe tener el formato de datos y si va a cifrar o no la base de datos.</span><span class="sxs-lookup"><span data-stu-id="fb6df-185">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="fb6df-186">Constante</span><span class="sxs-lookup"><span data-stu-id="fb6df-186">Constant</span></span></p></th>
<th><p><span data-ttu-id="fb6df-187">Description</span><span class="sxs-lookup"><span data-stu-id="fb6df-187">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-188"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-188"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-189">Crea una base de datos cifrada.</span><span class="sxs-lookup"><span data-stu-id="fb6df-189">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-190"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-190"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-191">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="fb6df-191">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-192"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-192"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-193">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.1.</span><span class="sxs-lookup"><span data-stu-id="fb6df-193">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-194"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-194"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-195">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 2.0.</span><span class="sxs-lookup"><span data-stu-id="fb6df-195">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-196"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-196"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-197">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 3.0 (compatible con la versión 3.5).</span><span class="sxs-lookup"><span data-stu-id="fb6df-197">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fb6df-198"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-198"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-199">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="fb6df-199">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fb6df-200"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="fb6df-200"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="fb6df-201">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Access versión 12.0.</span><span class="sxs-lookup"><span data-stu-id="fb6df-201">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="fb6df-202">Si omite la constante de cifrado, **CreateDatabase** crea una base de datos no cifrada.</span><span class="sxs-lookup"><span data-stu-id="fb6df-202">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="fb6df-p105">Utilice el método **CreateDatabase** para crear y abrir una nueva base de datos vacía y devolver el objeto **Database**. Debe completar su estructura y contenido con objetos DAO adicionales. Si desea crear una copia parcial o completa de una base de datos existente, puede utilizar el método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para crear una copia que pueda personalizar.</span><span class="sxs-lookup"><span data-stu-id="fb6df-p105">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

## <a name="example"></a><span data-ttu-id="fb6df-206">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb6df-206">Example</span></span>

<span data-ttu-id="fb6df-207">En este ejemplo se utiliza **CreateDatabase** para crear un nuevo objeto **Database** cifrado.</span><span class="sxs-lookup"><span data-stu-id="fb6df-207">This example uses **CreateDatabase** to create a new, encrypted **Database** object.</span></span>

```vb
    Sub CreateDatabaseX() 
     
       Dim wrkDefault As Workspace 
       Dim dbsNew As DATABASE 
       Dim prpLoop As Property 
     
       ' Get default Workspace. 
       Set wrkDefault = DBEngine.Workspaces(0) 
     
       ' Make sure there isn't already a file with the name of  
       ' the new database. 
       If Dir("NewDB.mdb") <> "" Then Kill "NewDB.mdb" 
     
       ' Create a new encrypted database with the specified  
       ' collating order. 
       Set dbsNew = wrkDefault.CreateDatabase("NewDB.mdb", _ 
          dbLangGeneral, dbEncrypt) 
     
       With dbsNew 
          Debug.Print "Properties of " & .Name 
          ' Enumerate the Properties collection of the new  
          ' Database object. 
          For Each prpLoop In .Properties 
             If prpLoop <> "" Then Debug.Print "  " & _ 
                prpLoop.Name & " = " & prpLoop 
          Next prpLoop 
       End With 
     
       dbsNew.Close 
     
    End Sub
```
