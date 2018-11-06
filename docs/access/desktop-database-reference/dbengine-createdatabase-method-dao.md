---
title: DBEngine.CreateDatabase (método) (DAO)
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
ms.openlocfilehash: e9c77eabfc0689c6696c4ea6c8b4998b6b345458
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998353"
---
# <a name="dbenginecreatedatabase-method-dao"></a><span data-ttu-id="e6238-102">DBEngine.CreateDatabase (método) (DAO)</span><span class="sxs-lookup"><span data-stu-id="e6238-102">DBEngine.CreateDatabase method (DAO)</span></span>

<span data-ttu-id="e6238-103">**Se aplica a**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6238-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6238-p101">Crea un nuevo objeto **[Database](database-object-dao.md)**, guarda la base de datos en disco y devuelve un objeto **Database** abierto (solo áreas de trabajo de Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e6238-p101">Creates a new **[Database](database-object-dao.md)** object, saves the database to disk, and returns an opened **Database** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="e6238-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6238-106">Syntax</span></span>

<span data-ttu-id="e6238-107">*expresión* . CreateDatabase (***nombre***, ***Configuración regional***, ***opción***)</span><span class="sxs-lookup"><span data-stu-id="e6238-107">*expression* .CreateDatabase(***Name***, ***Locale***, ***Option***)</span></span>

<span data-ttu-id="e6238-108">*expresión* Variable que representa un objeto **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="e6238-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6238-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6238-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6238-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="e6238-110">Name</span></span></p></th>
<th><p><span data-ttu-id="e6238-111">Obligatorio/opcional</span><span class="sxs-lookup"><span data-stu-id="e6238-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e6238-112">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="e6238-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="e6238-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6238-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6238-114"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="e6238-114"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="e6238-115">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e6238-115">Required</span></span></p></td>
<td><p><span data-ttu-id="e6238-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-117">Cadena de hasta 255 caracteres de longitud que es el nombre del archivo de base de datos que está creando.</span><span class="sxs-lookup"><span data-stu-id="e6238-117">A String up to 255 characters long that is the name of the database file that you're creating.</span></span> <span data-ttu-id="e6238-118">Puede ser el nombre de archivo y ruta de acceso completo.</span><span class="sxs-lookup"><span data-stu-id="e6238-118">It can be the full path and file name.</span></span> <span data-ttu-id="e6238-119">Si la red lo admite, también puede especificar una ruta de acceso de red, tales como &quot; \\server1\share1\dir1\db1&quot;.</span><span class="sxs-lookup"><span data-stu-id="e6238-119">If your network supports it, you can also specify a network path, such as &quot;\\server1\share1\dir1\db1&quot;.</span></span> <span data-ttu-id="e6238-120">Sólo se pueden crear archivos de base de datos de Microsoft Access con este método.</span><span class="sxs-lookup"><span data-stu-id="e6238-120">You can only create Microsoft Access database files with this method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-121"><em>Configuración regional</em></span><span class="sxs-lookup"><span data-stu-id="e6238-121"><em>Locale</em></span></span></p></td>
<td><p><span data-ttu-id="e6238-122">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="e6238-122">Required</span></span></p></td>
<td><p><span data-ttu-id="e6238-123"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-123"><strong>String</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="e6238-p103">Expresión de cadena que especifica un orden de intercalación para crear la base de datos, tal como se especifica en la sección de configuración. Debe proporcionar este argumento o se producirá un error.</span><span class="sxs-lookup"><span data-stu-id="e6238-p103">A string expression that specifies a collating order for creating the database, as specified in Settings. You must supply this argument or an error occurs.</span></span></p></li>
<li><p><span data-ttu-id="e6238-126">También puede crear una contraseña para el nuevo objeto <strong>Database</strong> concatenando la cadena de contraseña (comenzando por &quot;; pwd =&quot; ) con una constante en el argumento de <em>Configuración regional</em> , como la siguiente:</span><span class="sxs-lookup"><span data-stu-id="e6238-126">You can also create a password for the new <strong>Database</strong> object by concatenating the password string (starting with &quot;;pwd=&quot; ) with a constant in the <em>locale</em> argument, like this:</span></span></p></li>
<li><p><span data-ttu-id="e6238-127">dbLangSpanish &amp; &quot;; pwd = NuevaContraseña&quot;</span><span class="sxs-lookup"><span data-stu-id="e6238-127">dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="e6238-128">Si desea utilizar el argumento <em>locale</em> predeterminado, pero especificar una contraseña, sólo tiene que agregar una cadena de contraseña al argumento <em>locale</em>:</span><span class="sxs-lookup"><span data-stu-id="e6238-128">If you want to use the default <em>locale</em>, but specify a password, simply enter a password string for the <em>locale</em> argument:</span></span></p></li>
<li><p><span data-ttu-id="e6238-129">&quot;; pwd = NuevaContraseña&quot;</span><span class="sxs-lookup"><span data-stu-id="e6238-129">&quot;;pwd=NewPassword&quot;</span></span></p></li>
<li><p><span data-ttu-id="e6238-p104">[!NOTA] Use contraseñas seguras que combinen letras mayúsculas y minúsculas, números y símbolos. Las contraseñas que no son seguras no contienen una combinación de estos elementos. Contraseña segura: Y6dh!et5. Contraseña no segura: House27. Use una contraseña segura que pueda recordar para no tener que anotarla.</span><span class="sxs-lookup"><span data-stu-id="e6238-p104">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-135"><em>Opción</em></span><span class="sxs-lookup"><span data-stu-id="e6238-135"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="e6238-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="e6238-136">Optional</span></span></p></td>
<td><p><span data-ttu-id="e6238-137"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-137"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-p105">Constante o combinación de constantes que indican una o varias opciones, tal como se especifica en la sección de configuración. Puede combinar opciones sumando las constantes correspondientes.</span><span class="sxs-lookup"><span data-stu-id="e6238-p105">A constant or combination of constants that indicates one or more options, as specified in Settings. You can combine options by summing the corresponding constants.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="e6238-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6238-140">Remarks</span></span>

<span data-ttu-id="e6238-141">Puede utilizar alguna de las constantes siguientes para el argumento locale si desea especificar la propiedad **[CollatingOrder](database-collatingorder-property-dao.md)** de texto para comparaciones de cadenas.</span><span class="sxs-lookup"><span data-stu-id="e6238-141">You can use one of the following constants for the locale argument to specify the **[CollatingOrder](database-collatingorder-property-dao.md)** property of text for string comparisons.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6238-142">Constante</span><span class="sxs-lookup"><span data-stu-id="e6238-142">Constant</span></span></p></th>
<th><p><span data-ttu-id="e6238-143">Orden de intercalación</span><span class="sxs-lookup"><span data-stu-id="e6238-143">Collating order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6238-144"><strong>dbLangGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-144"><strong>dbLangGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-145">Inglés, alemán, francés, portugués, italiano y español (alfab. internacional)</span><span class="sxs-lookup"><span data-stu-id="e6238-145">English, German, French, Portuguese, Italian, and Modern Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-146"><strong>dbLangArabic</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-146"><strong>dbLangArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-147">Árabe</span><span class="sxs-lookup"><span data-stu-id="e6238-147">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-148"><strong>dbLangChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-148"><strong>dbLangChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-149">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="e6238-149">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-150"><strong>dbLangChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-150"><strong>dbLangChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-151">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="e6238-151">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-152"><strong>dbLangCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-152"><strong>dbLangCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-153">Ruso</span><span class="sxs-lookup"><span data-stu-id="e6238-153">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-154"><strong>dbLangCzech</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-154"><strong>dbLangCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-155">Checo</span><span class="sxs-lookup"><span data-stu-id="e6238-155">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-156"><strong>dbLangDutch</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-156"><strong>dbLangDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-157">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="e6238-157">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-158"><strong>dbLangGreek</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-158"><strong>dbLangGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-159">Griego</span><span class="sxs-lookup"><span data-stu-id="e6238-159">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-160"><strong>dbLangHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-160"><strong>dbLangHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-161">Hebreo</span><span class="sxs-lookup"><span data-stu-id="e6238-161">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-162"><strong>dbLangHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-162"><strong>dbLangHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-163">Húngaro</span><span class="sxs-lookup"><span data-stu-id="e6238-163">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-164"><strong>dbLangIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-164"><strong>dbLangIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-165">Islandés</span><span class="sxs-lookup"><span data-stu-id="e6238-165">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-166"><strong>dbLangJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-166"><strong>dbLangJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-167">Japonés</span><span class="sxs-lookup"><span data-stu-id="e6238-167">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-168"><strong>dbLangKorean</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-168"><strong>dbLangKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-169">Coreano</span><span class="sxs-lookup"><span data-stu-id="e6238-169">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-170"><strong>dbLangNordic</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-170"><strong>dbLangNordic</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-171">Idiomas nórdicos (sólo en la versión 1.0 del motor de base de datos de Microsoft Jet)</span><span class="sxs-lookup"><span data-stu-id="e6238-171">Nordic languages (Microsoft Jet database engine version 1.0 only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-172"><strong>dbLangNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-172"><strong>dbLangNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-173">Noruego y danés</span><span class="sxs-lookup"><span data-stu-id="e6238-173">Norwegian and Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-174"><strong>dbLangPolish</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-174"><strong>dbLangPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-175">Polaco</span><span class="sxs-lookup"><span data-stu-id="e6238-175">Polish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-176"><strong>dbLangSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-176"><strong>dbLangSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-177">Esloveno</span><span class="sxs-lookup"><span data-stu-id="e6238-177">Slovenian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-178"><strong>dbLangSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-178"><strong>dbLangSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-179">Español (alfab. tradicional)</span><span class="sxs-lookup"><span data-stu-id="e6238-179">Traditional Spanish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-180"><strong>dbLangSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-180"><strong>dbLangSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-181">Sueco y finés</span><span class="sxs-lookup"><span data-stu-id="e6238-181">Swedish and Finnish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-182"><strong>dbLangThai</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-182"><strong>dbLangThai</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-183">Tailandés</span><span class="sxs-lookup"><span data-stu-id="e6238-183">Thai</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-184"><strong>dbLangTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-184"><strong>dbLangTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-185">Turco</span><span class="sxs-lookup"><span data-stu-id="e6238-185">Turkish</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e6238-186">Puede utilizar una o varias de las constantes siguientes en el argumento options para especificar la versión que debe tener el formato de datos y si va a cifrar o no la base de datos.</span><span class="sxs-lookup"><span data-stu-id="e6238-186">You can use one or more of the following constants in the options argument to specify which version the data format should have and whether or not to encrypt the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6238-187">Constante</span><span class="sxs-lookup"><span data-stu-id="e6238-187">Constant</span></span></p></th>
<th><p><span data-ttu-id="e6238-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6238-188">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6238-189"><strong>dbEncrypt</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-189"><strong>dbEncrypt</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-190">Crea una base de datos cifrada.</span><span class="sxs-lookup"><span data-stu-id="e6238-190">Creates an encrypted database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-191"><strong>dbVersion10</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-191"><strong>dbVersion10</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-192">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.0.</span><span class="sxs-lookup"><span data-stu-id="e6238-192">Creates a database that uses the Microsoft Jet database engine version 1.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-193"><strong>dbVersion11</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-193"><strong>dbVersion11</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-194">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 1.1.</span><span class="sxs-lookup"><span data-stu-id="e6238-194">Creates a database that uses the Microsoft Jet database engine version 1.1 file format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-195"><strong>dbVersion20</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-195"><strong>dbVersion20</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-196">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 2.0.</span><span class="sxs-lookup"><span data-stu-id="e6238-196">Creates a database that uses the Microsoft Jet database engine version 2.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-197"><strong>dbVersion30</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-197"><strong>dbVersion30</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-198">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 3.0 (compatible con la versión 3.5).</span><span class="sxs-lookup"><span data-stu-id="e6238-198">Creates a database that uses the Microsoft Jet database engine version 3.0 file format (compatible with version 3.5).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6238-199"><strong>dbVersion40</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-199"><strong>dbVersion40</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-200">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Jet versión 4.0.</span><span class="sxs-lookup"><span data-stu-id="e6238-200">Creates a database that uses the Microsoft Jet database engine version 4.0 file format.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6238-201"><strong>dbVersion120</strong></span><span class="sxs-lookup"><span data-stu-id="e6238-201"><strong>dbVersion120</strong></span></span></p></td>
<td><p><span data-ttu-id="e6238-202">Crea una base de datos que utiliza el formato de archivo del motor de base de datos de Microsoft Access versión 12.0.</span><span class="sxs-lookup"><span data-stu-id="e6238-202">Creates a database that uses the Microsoft Access database engine version 12.0 file format.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e6238-203">Si omite la constante de cifrado, **CreateDatabase** crea una base de datos no cifrada.</span><span class="sxs-lookup"><span data-stu-id="e6238-203">If you omit the encryption constant, **CreateDatabase** creates an un-encrypted database.</span></span>

<span data-ttu-id="e6238-p106">Utilice el método **CreateDatabase** para crear y abrir una nueva base de datos vacía y devolver el objeto **Database**. Debe completar su estructura y contenido con objetos DAO adicionales. Si desea crear una copia parcial o completa de una base de datos existente, puede utilizar el método **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** para crear una copia que pueda personalizar.</span><span class="sxs-lookup"><span data-stu-id="e6238-p106">Use the **CreateDatabase** method to create and open a new, empty database, and return the **Database** object. You must complete its structure and content by using additional DAO objects. If you want to make a partial or complete copy of an existing database, you can use the **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** method to make a copy that you can customize.</span></span>

