---
title: Método DBEngine.CompactDatabase (DAO)
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
localization_priority: Priority
ms.openlocfilehash: b50cb0453df1fa357fbd0b089af2e74fdd4b4c1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294340"
---
# <a name="dbenginecompactdatabase-method-dao"></a><span data-ttu-id="1f692-102">Método DBEngine.CompactDatabase (DAO)</span><span class="sxs-lookup"><span data-stu-id="1f692-102">DBEngine.CompactDatabase method (DAO)</span></span>

<span data-ttu-id="1f692-103">**Se aplica a:** Access 2013 | Access 2016</span><span class="sxs-lookup"><span data-stu-id="1f692-103">**Applies to:** Access 2013 | Access 2016</span></span>

<span data-ttu-id="1f692-104">Copia y compacta una base de datos cerrada, y permite cambiar su versión, el orden de intercalación y el cifrado.</span><span class="sxs-lookup"><span data-stu-id="1f692-104">Copies and compacts a closed database, and gives you the option of changing its version, collating order, and encryption. (Microsoft Access workspaces only). .</span></span> <span data-ttu-id="1f692-105">(Solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1f692-105">(Microsoft Access workspaces only).</span></span>

> [!NOTE]
> <span data-ttu-id="1f692-106">Al usar tablas vinculadas cifradas para consultas de acción, actualización y SQL [como una instrucción SQL UPDATE (CurrentDb.Execute "UPDATE...")], debe proporcionar la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="1f692-106">When using encrypted linked tables for action, update, and SQL queries [such as a SQL UPDATE statement (CurrentDb.Execute "UPDATE...")], you must supply the encryption key.</span></span> <span data-ttu-id="1f692-107">Además, las tablas vinculadas tienen un límite de 19 caracteres para la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="1f692-107">Also, linked tables have a 19-character limit for the encryption key.</span></span> <span data-ttu-id="1f692-108">Consulte la sección **Tablas vinculadas cifradas** al final de este tema.</span><span class="sxs-lookup"><span data-stu-id="1f692-108">See the **Encrypted linked tables** section at the end of this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f692-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f692-109">Syntax</span></span>

<span data-ttu-id="1f692-110">*expression* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)</span><span class="sxs-lookup"><span data-stu-id="1f692-110">CompactDatabase(\*\*\*\*SrcName\*\*\*\*, ***DstName***, ***DstLocale, \*\*\*\*\*\*Options, \*\*\*\*\*\*password***)</span></span>

<span data-ttu-id="1f692-111">*expression* Expresión que devuelve un objeto **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="1f692-111">*expression*  An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="1f692-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="1f692-112">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f692-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="1f692-113">Name</span></span></p></th>
<th><p><span data-ttu-id="1f692-114">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="1f692-114">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="1f692-115">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="1f692-115">Data type</span></span></p></th>
<th><p><span data-ttu-id="1f692-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f692-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f692-117"><em>SrcName</em></span><span class="sxs-lookup"><span data-stu-id="1f692-117"><em>SrcName</em></span></span></p></td>
<td><p><span data-ttu-id="1f692-118">Necesario</span><span class="sxs-lookup"><span data-stu-id="1f692-118">Required</span></span></p></td>
<td><p><span data-ttu-id="1f692-119"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-119"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-120">Identifica una base de datos existente y cerrada.</span><span class="sxs-lookup"><span data-stu-id="1f692-120">Identifies an existing, closed database.</span></span> <span data-ttu-id="1f692-121">Puede ser una ruta de acceso completa y el nombre del archivo, como &quot;C:\db1.mdb&quot;.</span><span class="sxs-lookup"><span data-stu-id="1f692-121">It can be a full path and file name, such as "C:\db1.mdb".</span></span> <span data-ttu-id="1f692-122">Si el nombre de archivo tiene una extensión, debe especificarla.</span><span class="sxs-lookup"><span data-stu-id="1f692-122">If the file name has an extension, you must specify it.</span></span> <span data-ttu-id="1f692-123">Si la red lo admite, puede especificar también una ruta de red, como &quot;\\server1\share1\dir1\db1.mdb&quot;</span><span class="sxs-lookup"><span data-stu-id="1f692-123">If your network supports it, you can also specify a network path, such as "\\server1\share1\dir1\db1.mdb"</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-124"><em>DstName</em></span><span class="sxs-lookup"><span data-stu-id="1f692-124"><em>DstName</em></span></span></p></td>
<td><p><span data-ttu-id="1f692-125">Necesario</span><span class="sxs-lookup"><span data-stu-id="1f692-125">Required</span></span></p></td>
<td><p><span data-ttu-id="1f692-126"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-126"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-127">Nombre de archivo (y la ruta) de la base de datos compactada que va a crear.</span><span class="sxs-lookup"><span data-stu-id="1f692-127">the file name (and path) of the compacted database that you're creating.</span></span> <span data-ttu-id="1f692-128">Puede especificar también una ruta de red.</span><span class="sxs-lookup"><span data-stu-id="1f692-128">You can also specify a network path.</span></span> <span data-ttu-id="1f692-129">No puede utilizar este argumento para especificar el mismo archivo de base de datos que SrcName.</span><span class="sxs-lookup"><span data-stu-id="1f692-129">You can't use this  argument to specify the same database file as SrcName.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-130"><em>DstLocale</em></span><span class="sxs-lookup"><span data-stu-id="1f692-130"><em>DstLocale</em></span></span></p></td>
<td><p><span data-ttu-id="1f692-131">Opcional</span><span class="sxs-lookup"><span data-stu-id="1f692-131">Optional</span></span></p></td>
<td><p><span data-ttu-id="1f692-132"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-132"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-133">Expresión de cadena que especifica un orden de intercalación para crear DstName, como se especifica en Comentarios.</span><span class="sxs-lookup"><span data-stu-id="1f692-133">A string expression that specifies a collating order for creating DstName, as specified in Remarks.</span></span></p>
<ul>
<li><p><span data-ttu-id="1f692-134">Si omite este argumento, la configuración regional de DstName es la misma que la de SrcName.</span><span class="sxs-lookup"><span data-stu-id="1f692-134">If you omit this argument, the locale of DstName is the same as SrcName.</span></span></p></li>
<li><p><span data-ttu-id="1f692-135">Puede crear también una contraseña para DstName concatenando la cadena de contraseña (que empieza por &quot;;pwd=&quot;) con una constante en el argumento DstLocale, como la siguiente: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</span><span class="sxs-lookup"><span data-stu-id="1f692-135">You can also create a password for DstName by concatenating the password string (starting with ";pwd=") with a constant in the DstLocale argument, like this: dbLangSpanish & ";pwd=NewPassword".</span></span></p></li>
<li><p><span data-ttu-id="1f692-136">Si quiere utilizar el mismo DstLocale que SrcName (el valor predeterminado), pero especificar una nueva contraseña, solo tiene que especificar una cadena de contraseña para DstLocale: &quot;;pwd=NewPassword&quot;</span><span class="sxs-lookup"><span data-stu-id="1f692-136">If you want to use the same DstLocale as SrcName (the default value), but specify a new password, simply enter a password string for DstLocale: ";pwd=NewPassword"</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-137"><em>Opciones</em></span><span class="sxs-lookup"><span data-stu-id="1f692-137"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="1f692-138">Opcional</span><span class="sxs-lookup"><span data-stu-id="1f692-138">Optional</span></span></p></td>
<td><p><span data-ttu-id="1f692-139"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-139"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-p105">Opcional. Constante o combinación de constantes que indican una o varias opciones, tal como se ha especificado en los comentarios. Puede combinar opciones sumando las constantes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="1f692-p105">Optional. A constant or combination of constants that indicates one or more options, as specified in Remarks. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-143"><em>password</em></span><span class="sxs-lookup"><span data-stu-id="1f692-143"><em>Password</em></span></span></p></td>
<td><p><span data-ttu-id="1f692-144">Opcional</span><span class="sxs-lookup"><span data-stu-id="1f692-144">Optional</span></span></p></td>
<td><p><span data-ttu-id="1f692-145"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-145"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-146">Expresión de cadena que contiene una clave de cifrado, si la base de datos está cifrada.</span><span class="sxs-lookup"><span data-stu-id="1f692-146">A string expression containing an encryption key, if the database is encrypted.</span></span> <span data-ttu-id="1f692-147">La cadena &quot;;pwd=&quot; debe preceder a la contraseña real.</span><span class="sxs-lookup"><span data-stu-id="1f692-147">The string &quot;;pwd=&quot; must precede the actual password.</span></span> <span data-ttu-id="1f692-148">Si incluye una opción de contraseña en DstLocale, se omite esta configuración.</span><span class="sxs-lookup"><span data-stu-id="1f692-148">If you include a password setting in DstLocale, this setting is ignored.</span></span></p><p><span data-ttu-id="1f692-149"><strong>NOTA</strong>: este es un parámetro en desuso y no es compatible con el formato .ACCDB.</span><span class="sxs-lookup"><span data-stu-id="1f692-149"><strong>NOTE</strong>: This is deprecated parameter and is not supported in .ACCDB format.</span></span> <span data-ttu-id="1f692-150">Para cifrar un archivo .ACCDB, use la cadena de opción "pwd =".</span><span class="sxs-lookup"><span data-stu-id="1f692-150">To encrypt an .ACCDB file, use the "pwd=" option string.</span></span> <span data-ttu-id="1f692-151">Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos.</span><span class="sxs-lookup"><span data-stu-id="1f692-151">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols.</span></span> <span data-ttu-id="1f692-152">En las contraseñas no seguras estos elementos no se combinan.</span><span class="sxs-lookup"><span data-stu-id="1f692-152">Weak passwords don't mix these elements.</span></span> <span data-ttu-id="1f692-153">Contraseña segura: Y6dh!et5.</span><span class="sxs-lookup"><span data-stu-id="1f692-153">Strong password: Y6dh!et5.</span></span> <span data-ttu-id="1f692-154">Contraseña no segura: Casa27.</span><span class="sxs-lookup"><span data-stu-id="1f692-154">Weak password: House27.</span></span> <span data-ttu-id="1f692-155">Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="1f692-155">Use a strong password that you can remember so that you don't have to write it down.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1f692-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1f692-156">Remarks</span></span>

<span data-ttu-id="1f692-157">Puede usar una de las siguientes constantes para el argumento DstLocale para especificar la propiedad **CollatingOrder** para comparaciones de cadenas de texto.</span><span class="sxs-lookup"><span data-stu-id="1f692-157">You can use one of the following constants for the DstLocale argument to specify the **CollatingOrder** property for string comparisons of text.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f692-158">Constante</span><span class="sxs-lookup"><span data-stu-id="1f692-158">Constant</span></span></p></th>
<th><p><span data-ttu-id="1f692-159">Orden de intercalación</span><span class="sxs-lookup"><span data-stu-id="1f692-159">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f692-160"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-160"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-161">Inglés, alemán, francés, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="1f692-161">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-162"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-162"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-163">Árabe</span><span class="sxs-lookup"><span data-stu-id="1f692-163">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-164"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-164"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-165">chino simplificado</span><span class="sxs-lookup"><span data-stu-id="1f692-165">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-166"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-166"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-167">chino tradicional</span><span class="sxs-lookup"><span data-stu-id="1f692-167">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-168"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-168"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-169">Ruso</span><span class="sxs-lookup"><span data-stu-id="1f692-169">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-170"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-170"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-171">Checo</span><span class="sxs-lookup"><span data-stu-id="1f692-171">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-172"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-172"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-173">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="1f692-173">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-174"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-174"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-175">Griego</span><span class="sxs-lookup"><span data-stu-id="1f692-175">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-176"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-176"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-177">Hebreo</span><span class="sxs-lookup"><span data-stu-id="1f692-177">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-178"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-178"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-179">Húngaro</span><span class="sxs-lookup"><span data-stu-id="1f692-179">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-180"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-180"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-181">Islandés</span><span class="sxs-lookup"><span data-stu-id="1f692-181">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-182"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-182"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-183">Japonés</span><span class="sxs-lookup"><span data-stu-id="1f692-183">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-184"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-184"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-185">Coreano</span><span class="sxs-lookup"><span data-stu-id="1f692-185">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-186"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-186"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-187">Idiomas nórdicos (sólo en la versión 1.0 del motor de base de datos de Microsoft Jet)</span><span class="sxs-lookup"><span data-stu-id="1f692-187">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-188"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-188"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-189">Noruego y danés</span><span class="sxs-lookup"><span data-stu-id="1f692-189">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-190"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-190"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-191">Polaco</span><span class="sxs-lookup"><span data-stu-id="1f692-191">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-192"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-192"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-193">Esloveno</span><span class="sxs-lookup"><span data-stu-id="1f692-193">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-194"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-194"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-195">Español (alfab. tradicional)</span><span class="sxs-lookup"><span data-stu-id="1f692-195">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-196"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-196"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-197">Sueco y finlandés</span><span class="sxs-lookup"><span data-stu-id="1f692-197">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-198"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-198"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-199">Tailandés</span><span class="sxs-lookup"><span data-stu-id="1f692-199">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-200"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-200"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-201">Turco</span><span class="sxs-lookup"><span data-stu-id="1f692-201">Turkish</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1f692-202">Puede utilizar alguna de las constantes siguientes en el argumento options para especificar si va a cifrar o descifrar la base de datos mientras se compacta.</span><span class="sxs-lookup"><span data-stu-id="1f692-202">You can use one of the following constants in the options argument to specify whether to encrypt or to decrypt the database while it's compacted.</span></span>

> [!NOTE]
> <span data-ttu-id="1f692-203">La constantes dbEncrypt y dbDecrypt están en desuso y no se admiten en formatos de archivo .ACCDB.</span><span class="sxs-lookup"><span data-stu-id="1f692-203">The constants dbEncrypt and dbDecrypt are deprecated and not supported in .ACCDB file formats.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f692-204">Constante</span><span class="sxs-lookup"><span data-stu-id="1f692-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="1f692-205">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f692-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f692-206"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-206"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-207">Cifra la base de datos mientras se compacta.</span><span class="sxs-lookup"><span data-stu-id="1f692-207">Encrypt the database while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-208"><strong>dbDecrypt</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-208"><strong>dbDecrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-209">Descifrar la base de datos mientras se compacta.</span><span class="sxs-lookup"><span data-stu-id="1f692-209">Decrypt the database while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1f692-210">Si omite una constante de cifrado o si incluye **dbDecrypt** y **dbEncrypt**, DstName tendrá el mismo cifrado que SrcName.</span><span class="sxs-lookup"><span data-stu-id="1f692-210">If you omit an encryption constant or if you include both dbDecrypt and dbEncrypt, DstName will have the same encryption as SrcName.</span></span>

<span data-ttu-id="1f692-211">Puede utilizar alguna de las constantes siguientes en el argumento options para especificar la versión del formato de datos de la base de datos compactada.</span><span class="sxs-lookup"><span data-stu-id="1f692-211">You can use one of the following constants in the  options argument to specify the version of the data format for the compacted database.</span></span> <span data-ttu-id="1f692-212">Esta constante afecta únicamente a la versión del formato de datos de DstName y no a la versión de los objetos definidos por Microsoft Access, como formularios o informes.</span><span class="sxs-lookup"><span data-stu-id="1f692-212">This constant affects only the version of the data format of DstName and doesn't affect the version of any Microsoft Access-defined objects, such as forms and reports.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1f692-213">Constante</span><span class="sxs-lookup"><span data-stu-id="1f692-213">Constant</span></span></p></th>
<th><p><span data-ttu-id="1f692-214">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f692-214">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f692-215"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-215"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-216">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.0 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f692-216">Creates a database that uses the Microsoft Jet database engine version 1.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-217"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-217"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-218">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.1 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f692-218">Creates a database that uses the Microsoft Jet database engine version 1.1 file format while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-219"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-219"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-220">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 2.0 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f692-220">Creates a database that uses the Microsoft Jet database engine version 2.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-221"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-221"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-222">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 3.0 (compatible con la versión 3.5) mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f692-222">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5) while compacting.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1f692-223"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-223"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-224">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 4.0 mientras compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f692-224">Creates a database that uses the Microsoft Jet database engine version 4.0 file format while compacting.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1f692-225"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="1f692-225"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="1f692-226">Crea una base de datos que usa el formato de archivo de motor de base de datos Microsoft Access versión 12.0 mientras se compacta.</span><span class="sxs-lookup"><span data-stu-id="1f692-226">Creates a database that uses the Microsoft Access database engine version 12.0 file format while compacting.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="1f692-227">Solo puede especificar una constante de versión.</span><span class="sxs-lookup"><span data-stu-id="1f692-227">You can specify only one version constant.</span></span> <span data-ttu-id="1f692-228">Si se omite, DstName tendrá la misma versión que SrcName.</span><span class="sxs-lookup"><span data-stu-id="1f692-228">If you omit a version constant,  DstName will have the same version as  SrcName.</span></span> <span data-ttu-id="1f692-229">Sólo puede compactar DstName en una versión que sea la misma o superior a la de SrcName.</span><span class="sxs-lookup"><span data-stu-id="1f692-229">You can compact  DstName only to a version that is the same or later than that of  SrcName.</span></span>

<span data-ttu-id="1f692-p110">Cuando cambie los datos en una base de datos, el archivo de base de datos puede fragmentarse y utilizar más espacio en disco si es necesario. Puede utilizar el método **CompactDatabase** regularmente para compactar la base de datos y desfragmentar el archivo de base de datos. Las bases de datos compactadas suelen ser más pequeñas y ejecutarse más rápidamente. Puede cambiar también el orden de intercalación, el cifrado o la versión del formato de datos mientras copia y compacta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f692-p110">As you change data in a database, the database file can become fragmented and use more disk space than is necessary. Periodically, you can use the **CompactDatabase** method to compact your database to defragment the database file. The compacted database is usually smaller and often runs faster. You can also change the collating order, the encryption, or the version of the data format while you copy and compact the database.</span></span>

<span data-ttu-id="1f692-234">Debe cerrar SrcName antes de compactarla.</span><span class="sxs-lookup"><span data-stu-id="1f692-234">You must close  SrcName before you compact it.</span></span> <span data-ttu-id="1f692-235">En un entorno multiusuario, otros usuarios no pueden tener abierto SrcName mientras realiza la compactación.</span><span class="sxs-lookup"><span data-stu-id="1f692-235">In a multiuser environment, other users can't have  SrcName open while you're compacting it.</span></span> <span data-ttu-id="1f692-236">Si SrcName no está cerrado o no está disponible para uso exclusivo, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="1f692-236">If  SrcName isn't closed or isn't available for exclusive use, an error occurs.</span></span>

<span data-ttu-id="1f692-237">Como **CompactDatabase** crea una copia de la base de datos, debe disponer de espacio en disco suficiente para la base de datos original y duplicada.</span><span class="sxs-lookup"><span data-stu-id="1f692-237">Because **CompactDatabase** creates a copy of the database, you must have enough disk space for both the original and the duplicate databases.</span></span> <span data-ttu-id="1f692-238">La operación de compactación producirá un error si no hay espacio en disco suficiente.</span><span class="sxs-lookup"><span data-stu-id="1f692-238">The compact operation fails if there isn't enough disk space available.</span></span> <span data-ttu-id="1f692-239">La base de datos DstName duplicada no tiene que estar en el mismo disco que SrcName.</span><span class="sxs-lookup"><span data-stu-id="1f692-239">The  DstName duplicate database doesn't have to be on the same disk as  SrcName.</span></span> <span data-ttu-id="1f692-240">Una vez compactada correctamente la base de datos, puede eliminar el archivo SrcName y cambiar el nombre del archivo DstName compactado por el nombre de archivo original.</span><span class="sxs-lookup"><span data-stu-id="1f692-240">After successfully compacting a database, you can delete the  SrcName file and rename the compacted  DstName file to the original file name.</span></span>

<span data-ttu-id="1f692-241">El método **CompactDatabase** copia todos los datos y la configuración de permisos de seguridad de la base de datos especificada por SrcName en la base de datos especificada por DstName.</span><span class="sxs-lookup"><span data-stu-id="1f692-241">The CompactDatabase method copies all the data and the security permission settings from the database specified by  SrcName to the database specified by  DstName.</span></span>

> [!NOTE]
> <span data-ttu-id="1f692-242">Como el método **CompactDatabase** no convierte los objetos de Microsoft Access, no debería usar **CompactDatabase** para convertir una base de datos que contiene esos objetos.</span><span class="sxs-lookup"><span data-stu-id="1f692-242">Because the **CompactDatabase** method doesn't convert Microsoft Access objects, you shouldn't use **CompactDatabase** to convert a database containing such objects.</span></span>

## <a name="encrypted-linked-tables"></a><span data-ttu-id="1f692-243">Tablas vinculadas cifradas</span><span class="sxs-lookup"><span data-stu-id="1f692-243">Encrypted linked tables</span></span>

<span data-ttu-id="1f692-244">Las contraseñas con cifrado dependen del formato de archivo de la base de datos que está usando.</span><span class="sxs-lookup"><span data-stu-id="1f692-244">Encrypted passwords are dependent on the file format of the database that you are using.</span></span> <span data-ttu-id="1f692-245">Si usa una base de datos de Access 2003 (.mdb) o anterior, tendrá una contraseña para proteger la base de datos y una contraseña independiente para cifrar la base de datos.</span><span class="sxs-lookup"><span data-stu-id="1f692-245">If you are using an Access 2003 (.mdb) or earlier database, you will have one password to protect the database, and a separate password to encrypt the database.</span></span> <span data-ttu-id="1f692-246">En las bases de datos de Access 2007 (.accdb) y posteriores (.mdb), la única opción es cifrar y proteger la base de datos con una contraseña, ya que se ha quitado la opción de las dos contraseñas independientes.</span><span class="sxs-lookup"><span data-stu-id="1f692-246">For Access 2007 (.accdb) and later (.mdb) databases, the only option is to encrypt and protect the database with one password, as the option to have two separate passwords has been removed.</span></span>

> [!NOTE]
> <span data-ttu-id="1f692-247">En bases de datos de Access 2007 (.accdb), la contraseña es la clave de cifrado.</span><span class="sxs-lookup"><span data-stu-id="1f692-247">For Access 2007 (.accdb) databases, the password is the encryption key</span></span>

<span data-ttu-id="1f692-248">Puede usar el siguiente ejemplo de código VBA para un botón de comando:</span><span class="sxs-lookup"><span data-stu-id="1f692-248">You can use the following example VBA code for a command button:</span></span>

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

<span data-ttu-id="1f692-249">El ejemplo siguiente muestra cómo usar CompactDatabase con una contraseña (clave de cifrado) y, después, vincularla a una tabla de esa base de datos compactada.</span><span class="sxs-lookup"><span data-stu-id="1f692-249">The following code sample shows how to use CompactDatabase with a password (encryption key) and then link to a table in that compacted database.</span></span> <span data-ttu-id="1f692-250">Tenga en cuenta que debe proporcionar una contraseña.</span><span class="sxs-lookup"><span data-stu-id="1f692-250">Note that a password must be supplied.</span></span>

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
