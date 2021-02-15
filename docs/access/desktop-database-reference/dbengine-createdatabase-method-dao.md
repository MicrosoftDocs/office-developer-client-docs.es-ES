---
title: Método DBEngine.CreateDatabase (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 13e41dcd182f720b3611108311db6cd56fb4847e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294368"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="8615f-102">Método DBEngine.CreateDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="8615f-102">DBEngine.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="8615f-103">**Se aplica a:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8615f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8615f-104">Crea un nuevo objeto **[Database](database-object-dao.md)**, guarda la base de datos en el disco y devuelve un objeto **Database** abierto (sólo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8615f-104">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="8615f-105">.</span><span class="sxs-lookup"><span data-stu-id="8615f-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="8615f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8615f-106">Syntax</span></span>

<span data-ttu-id="8615f-107">*expresión* . CreateDatabase(***Name***, ***Locale***, ***Option***)</span><span class="sxs-lookup"><span data-stu-id="8615f-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="8615f-108">*expression* Variable que representa un objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="8615f-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="8615f-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="8615f-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8615f-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="8615f-110">Name</span></span></p></th>
<th><p><span data-ttu-id="8615f-111">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="8615f-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="8615f-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8615f-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="8615f-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8615f-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8615f-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="8615f-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="8615f-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8615f-115">Required</span></span></p></td>
<td><p><span data-ttu-id="8615f-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-117">String de hasta 255 caracteres de longitud que es el nombre del archivo de base de datos que va a crear.</span><span class="sxs-lookup"><span data-stu-id="8615f-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="8615f-118">Puede ser la ruta completa y el nombre del archivo.</span><span class="sxs-lookup"><span data-stu-id="8615f-118">It can be the full path and file name.</span></span> <span data-ttu-id="8615f-119">Si la red la admite, también puede especificar una ruta de acceso de red, como &quot; \\ server1\share1\dir1\db1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="8615f-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="8615f-120">Con este método sólo puede crear archivos de base de datos de Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="8615f-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-121"><em>Locale</em></span><span class="sxs-lookup"><span data-stu-id="8615f-121"><em>Locale</em></span></span></p></td>
<td><p><span data-ttu-id="8615f-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8615f-122">Required</span></span></p></td>
<td><p><span data-ttu-id="8615f-123"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="8615f-p103">Expresión de cadena que especifica un orden de intercalación para crear la base de datos, tal como se especifica en la sección de configuración. Debe proporcionar este argumento o se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="8615f-p103">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="8615f-126">También puede crear una contraseña para el nuevo objeto <strong>Database</strong> concatenando la cadena de contraseña (empezando por ;p wd= ) con una constante en el argumento de configuración regional, como &quot; &quot; esta: <em></em></span><span class="sxs-lookup"><span data-stu-id="8615f-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="8615f-127">dbLangSpanish &amp; &quot; ;p wd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="8615f-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="8615f-128">Si desea utilizar el argumento <em>locale</em> predeterminado, pero especificar una contraseña, sólo tiene que agregar una cadena de contraseña al argumento <em>locale</em>:</span><span class="sxs-lookup"><span data-stu-id="8615f-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="8615f-129">&quot;;p wd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="8615f-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="8615f-p104">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="8615f-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-135"><em>Opción</em></span><span class="sxs-lookup"><span data-stu-id="8615f-135"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="8615f-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="8615f-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="8615f-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-p105">Constante o combinación de constantes que indican una o varias opciones, tal como se especifica en la sección de configuración. Puede combinar opciones sumando las constantes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8615f-p105">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8615f-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8615f-140">Remarks</span></span>

<span data-ttu-id="8615f-141">Puede usar una de las siguientes constantes para el argumento de configuración regional para especificar la propiedad **[CollatingOrder](database-collatingorder-property-dao.md)** del texto para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="8615f-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8615f-142">Constante</span><span class="sxs-lookup"><span data-stu-id="8615f-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="8615f-143">Orden de intercalación</span><span class="sxs-lookup"><span data-stu-id="8615f-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8615f-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-145">Inglés, alemán, francés, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="8615f-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-147">Árabe</span><span class="sxs-lookup"><span data-stu-id="8615f-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-149">chino simplificado</span><span class="sxs-lookup"><span data-stu-id="8615f-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-151">chino tradicional</span><span class="sxs-lookup"><span data-stu-id="8615f-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-153">Ruso</span><span class="sxs-lookup"><span data-stu-id="8615f-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-155">Checo</span><span class="sxs-lookup"><span data-stu-id="8615f-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-157">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="8615f-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-159">Griego</span><span class="sxs-lookup"><span data-stu-id="8615f-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-161">Hebreo</span><span class="sxs-lookup"><span data-stu-id="8615f-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-163">Húngaro</span><span class="sxs-lookup"><span data-stu-id="8615f-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-165">Islandés</span><span class="sxs-lookup"><span data-stu-id="8615f-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-167">Japonés</span><span class="sxs-lookup"><span data-stu-id="8615f-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-169">Coreano</span><span class="sxs-lookup"><span data-stu-id="8615f-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-171">Idiomas nórdicos (sólo en la versión 1.0 del motor de base de datos de Microsoft Jet)</span><span class="sxs-lookup"><span data-stu-id="8615f-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-173">Noruego y danés</span><span class="sxs-lookup"><span data-stu-id="8615f-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-175">Polaco</span><span class="sxs-lookup"><span data-stu-id="8615f-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-177">Esloveno</span><span class="sxs-lookup"><span data-stu-id="8615f-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-179">Español (alfab. tradicional)</span><span class="sxs-lookup"><span data-stu-id="8615f-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-181">Sueco y finlandés</span><span class="sxs-lookup"><span data-stu-id="8615f-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-183">Tailandés</span><span class="sxs-lookup"><span data-stu-id="8615f-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-185">Turco</span><span class="sxs-lookup"><span data-stu-id="8615f-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8615f-186">Puede utilizar una o varias de las constantes siguientes en el argumento options para especificar la versión que debe tener el formato de datos y si va a cifrar o no la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8615f-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8615f-187">Constante</span><span class="sxs-lookup"><span data-stu-id="8615f-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="8615f-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="8615f-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8615f-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-190">Crea una base de datos cifrada.</span><span class="sxs-lookup"><span data-stu-id="8615f-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-192">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="8615f-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-194">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.1.</span><span class="sxs-lookup"><span data-stu-id="8615f-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-196">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 2.0.</span><span class="sxs-lookup"><span data-stu-id="8615f-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-198">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 3.0 (compatible con la versión 3.5).</span><span class="sxs-lookup"><span data-stu-id="8615f-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8615f-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-200">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="8615f-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8615f-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="8615f-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="8615f-202">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Access versión 12.0.</span><span class="sxs-lookup"><span data-stu-id="8615f-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8615f-203">Si omite la constante de cifrado, **CreateDatabase** crea una base de datos no cifrada.</span><span class="sxs-lookup"><span data-stu-id="8615f-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="8615f-p106">Utilice el método **CreateDatabase** para crear y abrir una nueva base de datos vacía y devolver el objeto **Database**. Debe completar su estructura y contenido con objetos DAO adicionales. Si desea crear una copia parcial o completa de una base de datos existente, puede utilizar el método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para crear una copia que pueda personalizar.</span><span class="sxs-lookup"><span data-stu-id="8615f-p106">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

