Changelog
=========

0.5.0
-----

* Adding ``FirstNameGenerator`` and ``LastNameGenerator``. Thanks to Jonathan
  Tien for the initial patch.
* Registered Autofixtures are used for models that are created for foreignkeys
  and many to many relations. Thanks to Theo Spears for the report.

0.4.0
-----

* Python 3 support! Though we had to drop Python 2.5 support. If you cannot
  upgrade to Python 2.6 by yet, please consider using the 0.3.x versions of
  django-autofixture.
  By the way: by Python 3 support, I mean, that the test suite is running
  without any errors. I have not tested yet the library in production for
  Python 3. So please test and submit bug reports if you encounter any.

0.3.2
-----

* ``DateTimeField`` receive timezone aware datetime objects now. Thanks to
  Scott Woodall for the report and patch.
* Adding ``static_domain`` parameter to ``EmailGenerator`` to allow the
  production of emails that will always have the same domain. Thanks to
  mvdwaeter for the initial patch.

0.3.1
-----

* ``field_values`` were not picked up if there was a default value assigned to
  the field. Thanks to sirex for the report.

0.3.0
-----

* Adding better support for subclassing ``AutoFixture`` through merging of
  nested ``Values`` classes.
* Renamed attribute and argument ``none_chance`` to better matching name ``empty_p`` for generators
  and ``none_p`` for ``AutoFixture``.
* Fixed some issues with management command options. Thanks Mikko Hellsing for
  his hard work.
* Fixed issues in unregister(). Thanks Mikko Hellsing for the report.
* Adding support for ``FloatField``. Thanks to Jyr Gaxiola for the report.

0.2.5
-----

* Fixing issue with ``--generate-fk`` option in management command. Thanks
  Mikko Hellsing for the `report and fix`_.

.. _report and fix: http://github.com/gregmuellegger/django-autofixture/issues/issue/1/

0.2.4
-----

* Using ``Autofixture.Values`` for defining initial values in ``Autofixture``
  subclasses.

* Making autodiscover more robust. Don't break if some module can't be
  imported or throws any other exception.

0.2.3
-----

* Fixing bug when a ``CharField`` with ``max_length`` smaller than 15 is used.

* ``AutoFixture.field_values`` accepts callables as values.
