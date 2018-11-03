---
title: DBEngine.CompactDatabase (método) (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e898a089843774792b1ed48cea65086331a94ec6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931221"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="8cad7-102">DBEngine.CompactDatabase (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="8cad7-102">DBEngine.CompactDatabase method (DAO)</span></span>

<span data-ttu-id="8cad7-103">**Se aplica a**: Access 2013 | Acceso 2016</span><span class="sxs-lookup"><span data-stu-id="8cad7-103">**Applies to**: Access 2013 | Access 2016</span></span>

<span data-ttu-id="8cad7-104">Copia y compacta una base de datos cerrada y ofrece la opción de cambiar su versión, de ordenación en orden y el cifrado.</span><span class="sxs-lookup"><span data-stu-id="8cad7-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption.</span></span> <span data-ttu-id="8cad7-105">(Sólo para áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="8cad7-105">(Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="8cad7-106">Cuando se usa el cifrado de las tablas vinculadas para acción, actualización y consultas SQL [por ejemplo, una instrucción UPDATE de SQL (CurrentDb.Execute "Actualizar...")], debe proporcionar la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="8cad7-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="8cad7-107">Además, las tablas vinculadas tienen un límite de 19 caracteres para la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="8cad7-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="8cad7-108">Vea la sección **Encrypted tablas vinculadas** al final de este tema.</span><span class="sxs-lookup"><span data-stu-id="8cad7-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cad7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cad7-109">Syntax</span></span>

<span data-ttu-id="8cad7-110">*expresión* . CompactDatabase (***SrcName***, ***DstName***, ***DstLocale***, ***Opciones***, ***contraseña***)</span><span class="sxs-lookup"><span data-stu-id="8cad7-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span></span>

<span data-ttu-id="8cad7-111">*expresión* Una expresión que devuelve un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="8cad7-111">*expression* An expression that returns a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="8cad7-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8cad7-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8cad7-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="8cad7-113">Name</span></span></p></th>
<th><p><span data-ttu-id="8cad7-114">Necesario/Opcional</span><span class="sxs-lookup"><span data-stu-id="8cad7-114">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="8cad7-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8cad7-115">Data Type</span></span></p></th>
<th><p><span data-ttu-id="8cad7-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cad7-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-117">SrcName</span><span class="sxs-lookup"><span data-stu-id="8cad7-117">SrcName</span></span></p></td>
<td><p><span data-ttu-id="8cad7-118">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8cad7-118">Required</span></span></p></td>
<td><p><span data-ttu-id="8cad7-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-120">Identifica una base de datos existente, cerrado.</span><span class="sxs-lookup"><span data-stu-id="8cad7-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="8cad7-121">Puede ser una ruta de acceso completa y el nombre de archivo, como &quot;C:\db1.mdb&quot;.</span><span class="sxs-lookup"><span data-stu-id="8cad7-121">It can be a full path and file name, such as &quot;C:\db1.mdb&quot;.</span></span> <span data-ttu-id="8cad7-122">Si el nombre de archivo tiene una extensión, debe especificar.</span><span class="sxs-lookup"><span data-stu-id="8cad7-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="8cad7-123">Si la red lo admite, también puede especificar una ruta de acceso de red, tales como &quot; \\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="8cad7-123">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1.mdb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-124">DstName</span><span class="sxs-lookup"><span data-stu-id="8cad7-124">DstName</span></span></p></td>
<td><p><span data-ttu-id="8cad7-125">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="8cad7-125">Required</span></span></p></td>
<td><p><span data-ttu-id="8cad7-126"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-127">el nombre de archivo (y la ruta) de la base de datos compactada que está creando.</span><span class="sxs-lookup"><span data-stu-id="8cad7-127">the file name (and path) of the compacted database that you're creating.</span></span> <span data-ttu-id="8cad7-128">También puede especificar una ruta de acceso de red.</span><span class="sxs-lookup"><span data-stu-id="8cad7-128">You can also specify a network path.</span></span> <span data-ttu-id="8cad7-129">No puede usar este argumento para especificar el mismo archivo de base de datos que SrcName.</span><span class="sxs-lookup"><span data-stu-id="8cad7-129">You can't use this argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-130">DstLocale</span><span class="sxs-lookup"><span data-stu-id="8cad7-130">DstLocale</span></span></p></td>
<td><p><span data-ttu-id="8cad7-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="8cad7-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="8cad7-132"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-133">Expresión de cadena que especifica un orden de intercalación para crear DstName, tal como se ha especificado en los comentarios.</span><span class="sxs-lookup"><span data-stu-id="8cad7-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="8cad7-134">Si se omite este argumento, la configuración regional de DstName es la misma que SrcName.</span><span class="sxs-lookup"><span data-stu-id="8cad7-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="8cad7-135">También puede crear una contraseña para DstName concatenando la cadena de contraseña (comenzando por &quot;; pwd =&quot;) con una constante en el argumento DstLocale, como la siguiente: dbLangSpanish &amp; &quot;; pwd = NuevaContraseña&quot;.</span><span class="sxs-lookup"><span data-stu-id="8cad7-135">You can also create a password for DstName by concatenating the password string (starting with &quot;;pwd=&quot;) with a constant in the DstLocale argument, like this: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span></span></p></li>
<li><p><span data-ttu-id="8cad7-136">Si desea utilizar el mismo DstLocale que SrcName (el valor predeterminado), pero especificar una nueva contraseña, introduzca simplemente una cadena de contraseña para DstLocale: &quot;; pwd = NuevaContraseña&quot;</span><span class="sxs-lookup"><span data-stu-id="8cad7-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: &quot;;pwd=NewPassword&quot;</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-137">Options</span><span class="sxs-lookup"><span data-stu-id="8cad7-137">Options</span></span></p></td>
<td><p><span data-ttu-id="8cad7-138">Opcional</span><span class="sxs-lookup"><span data-stu-id="8cad7-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="8cad7-139"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-p105">Opcional. Constante o combinación de constantes que indican una o varias opciones, tal como se ha especificado en los comentarios. Puede combinar opciones sumando las constantes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="8cad7-p105">Optional. A constant or combination of constants that indicates one or more options, as specified in Remarks. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-143">contraseña</span><span class="sxs-lookup"><span data-stu-id="8cad7-143">password</span></span></p></td>
<td><p><span data-ttu-id="8cad7-144">Opcional</span><span class="sxs-lookup"><span data-stu-id="8cad7-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="8cad7-145"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-146">Una expresión de cadena que contiene una clave de cifrado, si se cifra la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="8cad7-147">La cadena &quot;; pwd =&quot; deben preceder a la contraseña real.</span><span class="sxs-lookup"><span data-stu-id="8cad7-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="8cad7-148">Si incluye una opción de contraseña en DstLocale, este valor se omite.</span><span class="sxs-lookup"><span data-stu-id="8cad7-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p>

> [!NOTE]
> <span data-ttu-id="8cad7-149">Este parámetro en desuso es y no se admite en. Formato ACCDB.</span><span class="sxs-lookup"><span data-stu-id="8cad7-149">This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="8cad7-150">Para cifrar una. Archivo ACCDB, use la "pwd =" cadena de opción.</span><span class="sxs-lookup"><span data-stu-id="8cad7-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="8cad7-151">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="8cad7-152">Las contraseñas que no son seguras no contienen una combinación de estos elementos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="8cad7-153">Contraseña segura: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="8cad7-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="8cad7-154">Contraseña no segura: House27.</span><span class="sxs-lookup"><span data-stu-id="8cad7-154">Weak password: House27.</span></span> <span data-ttu-id="8cad7-155">Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="8cad7-155">Use a strong password that you can remember so that you don't have to write it down.</span></span>


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="8cad7-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cad7-156">Remarks</span></span>

<span data-ttu-id="8cad7-157">Puede utilizar alguna de las constantes siguientes para el argumento DstLocale si desea especificar la propiedad **CollatingOrder** para comparaciones de cadenas de texto.</span><span class="sxs-lookup"><span data-stu-id="8cad7-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8cad7-158">Constante</span><span class="sxs-lookup"><span data-stu-id="8cad7-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="8cad7-159">Orden de intercalación</span><span class="sxs-lookup"><span data-stu-id="8cad7-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-161">Inglés, alemán, francés, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="8cad7-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-163">Árabe</span><span class="sxs-lookup"><span data-stu-id="8cad7-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-165">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="8cad7-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-167">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="8cad7-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-169">Ruso</span><span class="sxs-lookup"><span data-stu-id="8cad7-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-171">Checo</span><span class="sxs-lookup"><span data-stu-id="8cad7-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-173">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="8cad7-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-175">Griego</span><span class="sxs-lookup"><span data-stu-id="8cad7-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-177">Hebreo</span><span class="sxs-lookup"><span data-stu-id="8cad7-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-179">Húngaro</span><span class="sxs-lookup"><span data-stu-id="8cad7-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-181">Islandés</span><span class="sxs-lookup"><span data-stu-id="8cad7-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-183">Japonés</span><span class="sxs-lookup"><span data-stu-id="8cad7-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-185">Coreano</span><span class="sxs-lookup"><span data-stu-id="8cad7-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-187">Idiomas nórdicos (sólo en la versión 1.0 del motor de base de datos de Microsoft Jet)</span><span class="sxs-lookup"><span data-stu-id="8cad7-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-189">Noruego y danés</span><span class="sxs-lookup"><span data-stu-id="8cad7-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-191">Polaco</span><span class="sxs-lookup"><span data-stu-id="8cad7-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-193">Esloveno</span><span class="sxs-lookup"><span data-stu-id="8cad7-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-195">Español (alfab. tradicional)</span><span class="sxs-lookup"><span data-stu-id="8cad7-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-197">Sueco y finés</span><span class="sxs-lookup"><span data-stu-id="8cad7-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-199">Tailandés</span><span class="sxs-lookup"><span data-stu-id="8cad7-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-201">Turco</span><span class="sxs-lookup"><span data-stu-id="8cad7-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="8cad7-202">Puede utilizar alguna de las constantes siguientes en el argumento options para especificar si va a cifrar o descifrar la base de datos mientras se compacta.</span><span class="sxs-lookup"><span data-stu-id="8cad7-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="8cad7-203">Las constantes dbEncrypt dbDecrypt en desuso y no se admite en. Formatos de archivo ACCDB.</span><span class="sxs-lookup"><span data-stu-id="8cad7-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8cad7-204">Constante</span><span class="sxs-lookup"><span data-stu-id="8cad7-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="8cad7-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cad7-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-207">Cifra la base de datos mientras se compacta.</span><span class="sxs-lookup"><span data-stu-id="8cad7-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-209">Descifra la base de datos mientras se compacta.</span><span class="sxs-lookup"><span data-stu-id="8cad7-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="8cad7-210">Si omite una constante de cifrado o si incluye **dbDecrypt** y **dbEncrypt**, DstName tendrá el mismo cifrado que SrcName.</span><span class="sxs-lookup"><span data-stu-id="8cad7-210">If you omit an encryption constant or if you include both **dbDecrypt** and **dbEncrypt**, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="8cad7-p108">Puede utilizar alguna de las constantes siguientes en el argumento options para especificar la versión del formato de datos de la base de datos compactada. Esta constante afecta únicamente a la versión del formato de datos de DstName y no a la versión de los objetos definidos por Microsoft Access, como formularios o informes.</span><span class="sxs-lookup"><span data-stu-id="8cad7-p108">You can use one of the following constants in the options argument to specify the version of the data format for the compacted database. This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8cad7-213">Constante</span><span class="sxs-lookup"><span data-stu-id="8cad7-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="8cad7-214">Descripción</span><span class="sxs-lookup"><span data-stu-id="8cad7-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-216">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.0 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-218">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.1 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-220">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 2.0 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-222">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 3.0 (compatible con la versión 3.5) mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8cad7-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-224">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 4.0 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8cad7-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="8cad7-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="8cad7-226">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Access versión 12.0 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="8cad7-227">Sólo puede especificar una constante de versión.</span><span class="sxs-lookup"><span data-stu-id="8cad7-227">You can specify only one version constant.</span></span> <span data-ttu-id="8cad7-228">Si omite una constante de versión, DstName tendrá la misma versión que SrcName.</span><span class="sxs-lookup"><span data-stu-id="8cad7-228">If you omit a version constant, DstName will have the same version as SrcName.</span></span> <span data-ttu-id="8cad7-229">Puede compactar DstName únicamente a una versión que es el mismo o posterior a la de SrcName.</span><span class="sxs-lookup"><span data-stu-id="8cad7-229">You can compact DstName only to a version that is the same or later than that of SrcName.</span></span>

<span data-ttu-id="8cad7-p110">Cuando cambie los datos en una base de datos, el archivo de base de datos puede fragmentarse y utilizar más espacio en disco si es necesario. Puede utilizar el método **CompactDatabase** regularmente para compactar la base de datos y desfragmentar el archivo de base de datos. Las bases de datos compactadas suelen ser más pequeñas y ejecutarse más rápidamente. Puede cambiar también el orden de intercalación, el cifrado o la versión del formato de datos mientras copia y compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-p110">As you change data in a database, the database file can become fragmented and use more disk space than is necessary. Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file. The compacted database is usually smaller and often runs faster. You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="8cad7-234">Debe cerrar SrcName antes de compactarlo.</span><span class="sxs-lookup"><span data-stu-id="8cad7-234">You must close SrcName before you compact it.</span></span> <span data-ttu-id="8cad7-235">En un entorno multiusuario, otros usuarios no pueden tener abierto SrcName mientras realiza la compactación.</span><span class="sxs-lookup"><span data-stu-id="8cad7-235">In a multiuser environment, other users can't have SrcName open while you're compacting it.</span></span> <span data-ttu-id="8cad7-236">Si SrcName no está cerrado o no está disponible para uso exclusivo, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="8cad7-236">If SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="8cad7-237">Como **CompactDatabase** crea una copia de la base de datos, debe disponer de espacio en disco suficiente para la base de datos original y duplicada.</span><span class="sxs-lookup"><span data-stu-id="8cad7-237">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases.</span></span> <span data-ttu-id="8cad7-238">La operación de compactación producirá un error si no hay espacio en disco suficiente.</span><span class="sxs-lookup"><span data-stu-id="8cad7-238">The compact operation fails if there isn't enough disk space available.</span></span> <span data-ttu-id="8cad7-239">La base de datos DstName duplicada no tiene que estar en el mismo disco que SrcName.</span><span class="sxs-lookup"><span data-stu-id="8cad7-239">The DstName duplicate database doesn't have to be on the same disk as SrcName.</span></span> <span data-ttu-id="8cad7-240">Después de compactar correctamente una base de datos, puede eliminar el archivo SrcName y cambie el nombre del archivo DstName compactado por el nombre del archivo original.</span><span class="sxs-lookup"><span data-stu-id="8cad7-240">After successfully compacting a database, you can delete the SrcName file and rename the compacted DstName file to the original file name.</span></span>

<span data-ttu-id="8cad7-241">El método **CompactDatabase** copia todos los datos y la configuración de permisos de seguridad de la base de datos especificada por SrcName en la base de datos especificada por DstName.</span><span class="sxs-lookup"><span data-stu-id="8cad7-241">The **CompactDatabase** method copies all the data and the security permission settings from the database specified by SrcName to the database specified by DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="8cad7-242">[!NOTA] Como el método **CompactDatabase** no convierte los objetos de Microsoft Access, no debe utilizar **CompactDatabase** para convertir una base de datos que contiene estos objetos.</span><span class="sxs-lookup"><span data-stu-id="8cad7-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="8cad7-243">Cifrar las tablas vinculadas</span><span class="sxs-lookup"><span data-stu-id="8cad7-243">Encrypted linked tables</span></span>

<span data-ttu-id="8cad7-244">Las contraseñas cifradas son dependientes en el formato de archivo de la base de datos que va a usar.</span><span class="sxs-lookup"><span data-stu-id="8cad7-244">Encrypted passwords are dependent on the file format of the database that you are using.</span></span> <span data-ttu-id="8cad7-245">Si está utilizando un Access 2003 (.mdb) o una base de datos anterior, tendrá una contraseña para proteger la base de datos y una contraseña para cifrar la base de datos independiente.</span><span class="sxs-lookup"><span data-stu-id="8cad7-245">If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database.</span></span> <span data-ttu-id="8cad7-246">Para Access 2007 (.accdb) y posterior bases de datos (.mdb), la única opción es cifrar y proteger la base de datos con una contraseña, tal y como se ha quitado la opción tener dos contraseñas distintas.</span><span class="sxs-lookup"><span data-stu-id="8cad7-246">For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="8cad7-247">Para las bases de datos de Access 2007 (.accdb), la contraseña es la clave de cifrado</span><span class="sxs-lookup"><span data-stu-id="8cad7-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="8cad7-248">Puede usar el siguiente ejemplo de código de VBA para un botón de comando:</span><span class="sxs-lookup"><span data-stu-id="8cad7-248">You can use the following example VBA code for a command button:</span></span>

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

<span data-ttu-id="8cad7-249">El ejemplo de código siguiente muestra cómo utilizar CompactDatabase con una contraseña (clave de cifrado) y, a continuación, vincular a una tabla en esa base de datos compactada.</span><span class="sxs-lookup"><span data-stu-id="8cad7-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="8cad7-250">Tenga en cuenta que se debe proporcionar una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8cad7-250">Note that a password must be supplied.</span></span>

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
